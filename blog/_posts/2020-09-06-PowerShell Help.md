---
layout: post  
title: PowerShell - Using the Help System
image: /assets/img/blog/help2.jpg
description: >
  Barely Scratching the surface with PowerShell's Basic Commands
---

Help is on the way
{:.figcaption}

- Table of Contents
{:toc}

## Objective :mag:

To document some use cases on how to the the [Help System](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/get-help?view=powershell-7){:target="_blank"} to find what you need in PowerShell

## Prerequisites :white_check_mark:

General Windows Operating System Knowledge

PowerShell version 5 or higher

## Using the PowerShell Help System

##### Update your PowerShell Help Files
   Ensures you have the latest help files
* Requires internet connection
* You may notice a few error messages while trying to update all of the modules. This is normal

```powershell	
	Update-Help
```

##### Get a list of Modules that support Updatable Help
	
```powershell	
Get-Module -ListAvailable | Where-Object -Property HelpInfoUri
```

##### Obtain full help file from on a specific cmdlet

```powershell
Get-Help Get-Service -Full
```

##### Get the online version of a help file (opens in a broser window)

```powershell
Get-Help Get-Process -Online
```

## Summary :clapper:
- Have a question?
- Find an error?
- Have a suggestion on how to improve this page?

##### Please leave a comment and I will respond back :speech_balloon:

<script src="https://utteranc.es/client.js"
        repo="djsimtech/blog"
        issue-term="pathname"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>