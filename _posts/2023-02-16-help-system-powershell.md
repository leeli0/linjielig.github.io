---
layout: post
title: Powershell help system 
date: 2023-02-15 16:13
categories: Windows
---

`Get-Help` it first searches for wildcard matches of command names based on the provided input. If it doesn't find a match, it searches through the help topics themselves, and if no match is found an error is returned.

`-Example`

`-Online`

`-Parameter Noun`

A parameter that doesn't require a value is called a switch parameter. When a switch parameter is specified, its value is true and when it's not, its value is false.
Parameter sets are mutually exclusive. 

positional parameter 

use the asterisk (*) wildcard character

PowerShell contains numerous conceptual (About) help topics.

`Get-Help About_*`

`Get-Command` is designed to help you locate commands.

`-Noun`

`-Name`

`-Name *service* -CommandType Cmdlet, Function, Alias`

`Update-Help`

`Save-Help`

`Get-Command | Get-Random | Get-Help -Online`

`Get-Member` helps you discover what objects, properties, and methods are available for commands.
The first line of the results in the previous example contains one piece of very important information. TypeName tells you what type of object was returned. 

`Get-Command -ParameterType TypeName`

`Get-Service -Name name | Select-Object -Property *`

`Get-Service -Name name | Select-Object -Property Status, Name, DisplayName, ServiceType`

`Get-Service -Name name | Get-Member -MemberType Method`

Format-* cmdlets

`(Get-Service -Name w32time).Stop()`

`Get-Service -Name w32time | Start-Service -PassThru`

object-base output

modules

variable

A PowerShell one-liner is one continuous pipeline and not necessarily a command that's on one physical line. Not all commands that are on one physical line are one-liners.

The Pipeline

NuGet repository