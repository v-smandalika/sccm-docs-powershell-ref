---
description: Installs a Configuration Manager client.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Install-CMClient
---

# Install-CMClient

## SYNOPSIS
Installs a Configuration Manager client.

## SYNTAX

### SearchByValueMandatory (Default)
```
Install-CMClient [-AlwaysInstallClient <Boolean>] [-ForceReinstall <Boolean>]
 [-IncludeDomainController <Boolean>] -InputObject <IResultObject> [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Install-CMClient [-AlwaysInstallClient <Boolean>] -DeviceId <String> [-ForceReinstall <Boolean>]
 [-IncludeDomainController <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Install-CMClient [-AlwaysInstallClient <Boolean>] -DeviceName <String> [-ForceReinstall <Boolean>]
 [-IncludeDomainController <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Install-CMClient [-AlwaysInstallClient <Boolean>] -CollectionId <String> [-ForceReinstall <Boolean>]
 [-IncludeDomainController <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Install-CMClient [-AlwaysInstallClient <Boolean>] [-ForceReinstall <Boolean>]
 [-IncludeDomainController <Boolean>] -Name <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Install-CMClient** cmdlet installs a client for Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Install a client
```
PS XYZ:\>Install-CMClient -Name "RemoteClient05" -SiteCode "CM1" -AlwaysInstallClient $True -IncludeDomainController $True
```

This command installs the client named RemoteClient05 on the Configuration Manager site that has the site code CM1.

## PARAMETERS

### -AlwaysInstallClient
Indicates whether Configuration Manager always installs the client.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the collection to which the client belongs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Specifies the ID for the device to which Configuration Manager installs the client.

```yaml
Type: String
Parameter Sets: SearchByDeviceIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of the device to which Configuration Manager installs the client.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory
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

### -ForceReinstall
Indicates whether the cmdlet reinstalls the client.

```yaml
Type: Boolean
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

### -IncludeDomainController
Indicates whether Configuration Manager authenticates and authorizes the client by using the clients domain controller.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a Configuration Manager client object.
You can get a Configuration Manager client object by using the [Get-CMBaseline](Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Collection, Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager client.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts this site system role.

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

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)

[Update-CMClientStatus](Update-CMClientStatus.md)

[Get-CMDevice](Get-CMDevice.md)

[Get-CMBaseline](Get-CMBaseline.md)
