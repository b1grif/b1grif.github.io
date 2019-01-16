---
layout: post
title: Pester Testdrive
---

I had one of those light bulb moments today. I've been struggling through creating Pester tests off and on for a while 
now and one of the sticking points was TestDrive. Well I dont know if I didnt read the documentation close enough or 
what but I realized today that maybe Pester was creating the temp drive but my tests were failing because of the folder 
structure. So I created ended up with this in my Describe block:

```
$TestPath = "TestDrive:\Test"

if (!(Test-Path $TestPath)){
    New-Item -Path $TestPath -ItemType Directory
}
```
And everything worked! I guess I had assumed that TestDrive would create the entire folder structure but that isn't the 
case. So hopefully this can help someone else out there get to creating successful tests quicker!
