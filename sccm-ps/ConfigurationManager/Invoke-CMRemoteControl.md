---
description: Enables remote control on computers.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMRemoteControl
---

# Invoke-CMRemoteControl

## SYNOPSIS
Enables remote control on computers.

## SYNTAX

### InvokeDeviceByValueMandatory (Default)
```
Invoke-CMRemoteControl -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByIdMandatory
```
Invoke-CMRemoteControl -DeviceId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByNameMandatory
```
Invoke-CMRemoteControl -DeviceName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeSiteStatusByNameMandatory
```
Invoke-CMRemoteControl [-PassThru] [-SiteCode <String>] [-SiteSystemRole <String>]
 -SiteSystemServerName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMRemoteControl** cmdlet enables remote control on the computers that you want to use in a remote control session.
You can enable remote control on computers by specifying the ID or name of the computers, the site systems, or the site status.

Use remote control in Configuration Manager to remotely administer, provide assistance, or view any client computer in the hierarchy.
You can use remote control to troubleshoot hardware and software configuration problems on client computers and to provide help desk support when access to the computer of a user is required.
Configuration Manager supports the remote control of workgroup computers and computers that are joined to an Active Directory domain.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Enable remote control on a computer
```
PS XYZ:\>Invoke-CMRemoteControl -DeviceName "CMCEN-DIST02"
```

This command enables remote control on the computer named CMCEN-DIST02.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: InvokeDeviceByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String
Parameter Sets: InvokeDeviceByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: InvokeDeviceByValueMandatory
Aliases: Device, SiteStatus

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies an array of site codes of Configuration Manager sites that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemRole
Specifies an array of Configuration Manager roles that the site system performs.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases: Role

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMDevice](Get-CMDevice.md)

[Get-CMSiteStatusMessage](Get-CMSiteStatusMessage.md)
