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

To provide some very basic PowerShell commands that will get you started on your journey to scripting and automation.

## Prerequisites :white_check_mark:

General Windows Operating System Knowledge

PowerShell version 5 or higher

We'll cover how to check your PowerShell version below
{:.note}

## Background :bulb:

##### Q: What exactly is [PowerShell?](https://docs.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7)

A: PowerShell is a cross-platform task automation and configuration management framework, consisting of a command-line shell and scripting language.

##### Q: How Do I open PowerShell?

Windows PowerShell comes included with Windows
 - Option 1: Hit the Start button (On Windows 10) and start typing "PowerShell". You can open it normally or right click and open as an Administrator
 - Option 2: On the Keyboard hold down the "Windows Key + R" to bring up a run command. Type "PowerShell" and hit enter
 - Option 3: In File Explorer, navigate to C:\Windows\System32\WindowsPowerShell\v1.0 and double click the powershell.exe icon.
 - Like everything in Windows there are a dozen ways to accomplish the same task, so this is not an all-inclusive list. If you have a favorite way of opening PowerShell, let others know if the comments and I will add it to the list.

## How to Enter Commands

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

##### Q: I'm used to running commands in the Command Prompt. Will those commands run in PowerShell too?

A: In most cases yes. IpConfig and Ping are .exe's and PowerShell can run those without issue:

Running [IPConfig](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/ipconfig) in PowerShell:

```Powershell
PS C:\> ipconfig.exe                                                                                       
Windows IP Configuration

Ethernet adapter vEthernet (External vSwitch):

   Connection-specific DNS Suffix  . :
   IPv4 Address. . . . . . . . . . . : 192.168.1.119
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 192.168.1.1

PS C:\>                                
```

Running a ping test on Google

```powershell
PS C:\> ping www.google.com                                                                                
Pinging www.google.com [142.250.68.4] with 32 bytes of data:
Reply from 142.250.68.4: bytes=32 time=26ms TTL=119
Reply from 142.250.68.4: bytes=32 time=18ms TTL=119
Reply from 142.250.68.4: bytes=32 time=19ms TTL=119
Reply from 142.250.68.4: bytes=32 time=19ms TTL=119

Ping statistics for 142.250.68.4:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 18ms, Maximum = 26ms, Average = 20ms
```

## External Links :link:

[Microsoft PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)

[PowerShell.org](https://powershell.org/)

[Top PowerShell Blogs for 2020](https://blog.feedspot.com/powershell_blogs/)

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
