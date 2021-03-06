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
title: Get-AdfsWebApiApplication
ms.assetid: CC8998A0-12E0-4CBA-A56B-FBFC5F399AA2
---

# Get-AdfsWebApiApplication

## SYNOPSIS
Gets Web API application roles in AD FS.

## SYNTAX

### Identifier (Default)
```
Get-AdfsWebApiApplication [[-Identifier] <String[]>] [<CommonParameters>]
```

### Name
```
Get-AdfsWebApiApplication [-Name] <String[]> [<CommonParameters>]
```

### PrefixIdentifier
```
Get-AdfsWebApiApplication [-PrefixIdentifier] <String> [<CommonParameters>]
```

### ApplicationObject
```
Get-AdfsWebApiApplication [-Application] <WebApiApplication> [<CommonParameters>]
```

### ApplicationGroupIdentifier
```
Get-AdfsWebApiApplication [-ApplicationGroupIdentifier] <String> [<CommonParameters>]
```

### ApplicationGroupObject
```
Get-AdfsWebApiApplication [-ApplicationGroup] <ApplicationGroup> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AdfsWebApiApplication** cmdlet gets Web API application roles in Active Directory Federation Services (AD FS).

## EXAMPLES


## PARAMETERS

### -Application
Specifies a Web API application to get.

```yaml
Type: WebApiApplication
Parameter Sets: ApplicationObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationGroup
Specifies an application group for which to get Web API applications.

```yaml
Type: ApplicationGroup
Parameter Sets: ApplicationGroupObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationGroupIdentifier
Specifies the ID of an application group for which to get Web API applications.

```yaml
Type: String
Parameter Sets: ApplicationGroupIdentifier
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Identifier
Specifies an ID of a Web API application to get.

```yaml
Type: String[]
Parameter Sets: Identifier
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of Web API applications to get.

```yaml
Type: String[]
Parameter Sets: Name
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrefixIdentifier
Specifies the prefix identifier of Web API applications to get.

```yaml
Type: String
Parameter Sets: PrefixIdentifier
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]
Microsoft.IdentityServer.Management.Resources.WebApiApplication
System.String
Microsoft.IdentityServer.Management.Resources.ApplicationGroup

## OUTPUTS

	Get-AdfsWebApiApplication
	Microsoft.IdentityServer.Management.Resources.WebApiApplication
	{get;}         AccessControlPolicyName                           string
	{get;}         AccessControlPolicyParameters                     System.Object
	{get;}         AdditionalAuthenticationRules                     string
	{get;}         AllowedAuthenticationClassReferences              string[]
	{get;set;}     AllowedClientTypes                                Microsoft.IdentityServer.Protocols.PolicyStore.AllowedClientTypes
	{get;}         AlwaysRequireAuthentication                       bool
	{get;}         ApplicationGroupId                                string
	{get;}         ApplicationGroupIdentifier                        string
	{get;}         ClaimsProviderName                                string[]
	{get;set;}     DelegationAuthorizationRules                      string
	{get;set;}     Description                                       string
	{get;}         Enabled                                           bool
	{get;}         Identifier                                        System.Collections.ObjectModel.ReadOnlyCollection[string]
	{get;set;}     ImpersonationAuthorizationRules                   string
	{get;set;}     IssuanceAuthorizationRules                        string
	{get;set;}     IssuanceTransformRules                            string
	{get;}         IssueOAuthRefreshTokensTo                         Microsoft.IdentityServer.Protocols.PolicyStore.RefreshTokenIssuanceDeviceTypes
	{get;set;}     Name                                              string
	{get;}         NotBeforeSkew                                     int
	{get;}         PublishedThroughProxy                             bool
	{get;set;}     RefreshTokenProtectionEnabled                     bool
	{get;}         RequestMFAFromClaimsProviders                     bool
	{get;}         ResultantPolicy                                   Microsoft.IdentityServer.PolicyModel.Configuration.PolicyTemplate.PolicyMetadata
	{get;}         TokenLifetime                                     int
	---------------------------
	
	
	
	(Get-AdfsWebApiApplication | select AllowedClientTypes)
	public enum AllowedClientTypes
	    {
	        None = 0,
	        Public = 2,
	        Confidential=4,
	    }
	---------------------------
	
	
	
	(Get-AdfsWebApiApplication | select IssueOAuthRefreshTokensTo)
	public enum RefreshTokenIssuanceDeviceTypes
	    {
	        NoDevice = 0,
	        WorkplaceJoinedDevices = 1,
	        AllDevices = 2
	    }
	---------------------------
	
	
	
	(Get-AdfsWebApiApplication | select ResultantPolicy)
	Microsoft.IdentityServer.PolicyModel.Configuration.PolicyTemplate.PolicyMetadata
	{get;}         IsParameterized                                   bool
	{get;}         Serialized                                        string
	{get;}         Summary                                           string
	---------------------------

## NOTES

## RELATED LINKS

[Add-AdfsWebApiApplication](./Add-AdfsWebApiApplication.md)

[Remove-AdfsWebApiApplication](./Remove-AdfsWebApiApplication.md)

[Set-AdfsWebApiApplication](./Set-AdfsWebApiApplication.md)

