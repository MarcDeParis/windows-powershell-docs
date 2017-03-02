---
ms.mktglfcycl: manage
ms.sitesec: library
ms.author: brianlic
author: brianlic-msft
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.IdentityServer.Management.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: w10
ms.technology: powershell-windows
ms.topic: reference
online version: 
schema: 2.0.0
title: New-AdfsContactPerson
ms.assetid: BFFB3E1F-061F-46FE-8507-F85F86ED8016
---

# New-AdfsContactPerson

## SYNOPSIS
Creates a contact person object.

## SYNTAX

```
New-AdfsContactPerson [-Company <String>] [-EmailAddress <String[]>] [-GivenName <String>]
 [-TelephoneNumber <String[]>] [-Surname <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AdfsContactPerson** cmdlet creates a contact person object in ADFS.

## EXAMPLES

### Example 1: Create and publish contact person object
```
PS C:\> $CP = New-AdfsContactPerson -EmailAddress "support@fabrikam.com"
PS C:\> Set-AdfsProperties -ContactPerson $CP
```

The first command creates a contact person who has the specified address, and then assigns it to the $CP variable.

The second command uses the **Set-AdfsProperties** cmdlet to publish the contact person object to the Federation Service.

## PARAMETERS

### -Company
Specifies the company name of the contact person.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAddress
Specifies an array of e-mail addresses of the contact person.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GivenName
Specifies the given name of the contact person.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Surname
Specifies the surname, or last name, of the contact person.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TelephoneNumber
Specifies an array of telephone numbers of the contact person.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.IdentityServer.PowerShell.Resources.ContactPerson
This cmdlet generates a class structure that represents a contact person object in the Federation Service.

## NOTES
* You can publish this contact person in the federation metadata of the Federation Service by using the **Set-AdfsProperties** cmdlet.

## RELATED LINKS

[Get-AdfsProperties](./Get-AdfsProperties.md)

[Set-AdfsProperties](./Set-AdfsProperties.md)
