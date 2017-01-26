---
author: brianlic-msft
description: 
external help file: Microsoft.Licensing.VolumeActivation.Powershell.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Initialize-VamtData
ms.assetid: 6DF25E18-FC39-42E2-B616-1EC5EE860ED6
---

# Initialize-VamtData

## SYNOPSIS
Initializes the VAMT database and removes all the data.

## SYNTAX

```
Initialize-VamtData [-PreserveKeys] [-DbConnectionString <String>] [-Confirm] [-DbCommandTimeout <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Initialize-VamtData** cmdlet restores a dep_nextref_vamt database to its initial state and removes all the data from the database.
You can preserve the product keys in the database if you need them.
You can also suppress the prompt that asks you to confirm the database initialization.

## EXAMPLES

### Example 1: Initialize database and preserve keys
```
PS C:\>Initialize-VamtData -PreserveKeys
```

This command initializes the database, but retains the product keys.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DbCommandTimeout
Indicates how long dep_nextref_vamt waits for a response from the database before timing out.
The default value is 30 seconds.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DbConnectionString
Specifies the database to be initialized.
If no database connection string is provided, dep_nextref_vamt attempts to use the database that the dep_nextref_vamt user console used on the local computer.
If dep_nextref_vamt does not find a database, it returns an error.
You can find the connection string in the dep_nextref_vamt UI in the Preferences dialog box.
On the menu bar, click View, and then click Preferences to open the Volume Activation Management Tool Preferences dialog box.
The connection string is in the Database Settings section under Current connection string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PreserveKeys
Indicates that the product keys in the dep_nextref_vamt database will be retained when the database is initialized.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Import-VamtData](./Import-VamtData.md)

[Export-VamtData](./Export-VamtData.md)
