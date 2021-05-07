---
layout: post  
title: PowerShell Tips
image: /assets/img/blog/Tips.jpg
description: >
  Useful PowerShell Tips
---

Useful PowerShell Tips
{:.figcaption}

- Table of Contents
{:toc}

## Objective :mag:

To document some useful PowerShell tips that I've come across.

## Prerequisites :white_check_mark:

General Windows Operating System Knowledge

PowerShell version 5 or higher

## Useful PowerShell Tips

##### Check if PowerShell is running in 32-bit or 64-bit process.

Method #1
* If output = True, PowerShell is running as a 64-bit Process

```powershell
[System.Environment]::Is64BitProcess
```

Method #2
* If output = 8, PowerShell is running as a 64-bit Process
* If output = 4, PowerShell is running as a 32-bit Process

```powershell	
[intptr]::size
```

##### Check Powershell Version

```powershell
$PSVersionTable
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
