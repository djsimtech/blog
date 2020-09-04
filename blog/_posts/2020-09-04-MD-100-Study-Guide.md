---
layout: post
title: Microsoft MD-100 Certification - Study Guide
image: /assets/img/blog/MD-100.jpg
description: >
  Links to help you study for and pass the Microsoft MD-100 Certification Test
---


Microsoft 365 Certified - Modern Desktop Administrator - Associate
{:.figcaption}

- Table of Contents
{:toc}

## Objective

To provide a one-stop shop for all the topics covered on the Microsoft MD-100 Certification exam.

## Prerequisites

General Windows Operating System Knowledge

(Optional) Account at the Microsoft Learn site to track progress [Click Here to create an account](https://docs.microsoft.com/en-us/learn/)

## Background

Modern Desktop Administrators deploy, configure, secure, manage, and monitor devices and client applications in an enterprise environment.

## PowerShell One-Liners

### Time of the Last Reboot

```powershell
(Get-CimInstance Win32_OperatingSystem).LastBootUpTime
```

### Find Your Public IP Address

```powershell
(Invoke-RestMethod ipinfo.io/json).ip
```

### Find Domain Controllers on Your Domain

```powershell
Resolve-DnsName -Type ALL -Name _ldap._tcp.dc._msdcs.$env:userdnsdomain
```

### List Software Available for Uninstall

```powershell
Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\* | Select-Object DisplayName, DisplayVersion, Publisher, InstallDate | Format-Table
```

### Install PowerShell Core (6 and 7)

```powershell
Invoke-Expression "& { $(Invoke-RestMethod -Uri aka.ms/install-powers…) }" -UseMSI -Preview
```

### Get Free Space for System Drive

```powershell
(Get-PSDrive $Env:SystemDrive.Trim(':')).Free/1GB
```

### Get Parent Process(es)

```powershell
foreach ($prid in ($ppid = foreach ($process in (Get-Process -Name "powershell")) { (Get-CimInstance Win32_Process | Where-Object processid -EQ $process.Id).parentprocessid })) { Get-Process -Id $prid }
```

### List Subdirectories in the Current Directory

```powershell
Get-ChildItem -Directory
```

### List Started Services

```powershell
Get-Service | Where-Object {$_.status -eq "Started"}
```

### Tail (grep) a File

```powershell
Get-Content ./logfile.log -Tail 5 –Wait
```

### Port Scanner

```powershell
0..65535 | Foreach-Object { Test-NetConnection -Port $_ scanme.nmap.org -WA SilentlyContinue | Format-Table -Property ComputerName,RemoteAddress,RemotePort,TcpTestSucceeded }
```

### Common WMI (CIM) Queries

```powershell
# BIOS Version
(Get-CimInstance Win32_BIOS).SMBIOSBIOSVersion

# Serial Number
(Get-CimInstance Win32_BIOS).SerialNumber

# Model
(Get-CimInstance Win32_ComputerSystem).Model

# Printers
Get-CimInstance Win32_Printer | Select-Object Name, PortName, Default

# Active Directory Domain
(Get-CimInstance Win32_ComputerSystem).Domain
```

### Cat Facts

```powershell
Invoke-WebRequest -Uri 'https://catfact.ninja/fact' -UseBasicParsing | Select-Object -ExpandProperty 'Content' | ConvertFrom-Json | Select-Object -ExpandProperty fact
```

### Get a Random XKCD Comic

```powershell
Invoke-RestMethod "http://xkcd.com/$(Get-Random -min 0 -max 2000)/info.0.json" | Select-Object title, transcript, alt, img | Format-List
```

## Conclusion

Hopefully, you've found some snippets in this post useful. For me, one-liners
have been fun, interactive ways to play with PowerShell and test my knowledge,
expectations, and push the language to its limits.

Have a cool one-liner you'd like to add to this doc? Feel free to drop a comment
or edit this page directly on GitHub using the button below.

Want more one-liners? [Click
here](https://parade.com/1040121/marynliles/one-liners/).

/dadjoke 🙃

## Related Links

- [What’s a PowerShell One-Liner & NOT a PowerShell One-Liner?](https://mikefrobbins.com/2019/02/07/whats-a-powershell-one-liner-not-a-powershell-one-liner/)
- [PowerShell One-Liners: Help, Syntax, Display and Files](https://www.red-gate.com/simple-talk/sysadmin/powershell/powershell-one-liners-help-syntax-display-and-files/)

<script src="https://utteranc.es/client.js"
        repo="djsimtech/blog"
        issue-term="pathname"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>