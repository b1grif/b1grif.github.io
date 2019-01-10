---
layout: post
title: Admin System Details
---

## Admin Systems Details 
Our admin system is sent to us as a collection of files that are supposed to be copied and deployed manually...
as we know this might work fine for a very small environment but we need this process to scale to 15 application servers.
In the beginning we were deploying this manually to each of these servers which would take on average 30 - 40 minutes. 
But wait...that was only if you didnt make any mistakes. If you missed a step that could mean that you didnt get a
backup or one of the new pieces of the application wasn't installed. Powershell to the rescue! I created one 1700 line
script 
