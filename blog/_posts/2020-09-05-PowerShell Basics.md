---
layout: post  
title: PowerShell - The Very Basics
image: /assets/img/blog/psride.jpg
description: >
  Barely Scratching the surface with PowerShell's Basic Commands
---

Buckle Up....You're in for a wild ride!
{:.figcaption}

- Table of Contents
{:toc}

## Objective :mag:

To document some very basic PowerShell commands that I have learned so I can keep them in one place.

## Prerequisites :white_check_mark:

General Windows Operating System Knowledge

PowerShell version 5 or higher (Command below will show what version is running)

## Background :bulb:

##### Q: What exactly is [PowerShell?](https://docs.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7)

A: According to Microsoft, PowerShell is a cross-platform task automation and configuration management framework, consisting of a command-line shell and scripting language.

##### Q: How Do I open PowerShell?

Windows PowerShell comes included with Windows
 - Option 1: Hit the Start button (On Windows 10) and start typing "PowerShell". You can open it normally or right click and open as an Administrator
 - Option 2: On the Keyboard hold down the "Windows Key + R" to bring up a run command. Type "PowerShell" and hit enter
 - Option 3: In File Explorer, navigate to C:\Windows\System32\WindowsPowerShell\v1.0 and double click the powershell.exe icon.
 - Like everything in Windows there are a dozen ways to accomplish the same task, so this is not an all-inclusive list. If you have a favorite way of opening PowerShell, let others know if the comments and I will add it to the list.

## How to Enter Commands :computer:

##### Q: How Can I check which version of PowerShell I am running?

A: Open a powershell console window and enter the following command

```powershell
PS C:\> $PSVersionTable.psversion                                                                          
Major  Minor  Build  Revision
-----  -----  -----  --------
5      1      18362  752
```

By looking at the "Major" and "Minor" columns, you can see that in this scenario, PowerShell is on Version 5.1
{:.note}

##### Q: How do you enter commands in PowerShell?

A: You enter commands using a Verb-Noun syntax. Four examples below show the format used.

* Get-EventLog
* Format-Table
* Get-Process
* Stop-Process

## External Links :link:

[Microsoft PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/){:target="_blank"}

[PowerShell.org](https://powershell.org/){:target="_blank"}

[Top PowerShell Blogs for 2020](https://blog.feedspot.com/powershell_blogs/){:target="_blank"}

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
