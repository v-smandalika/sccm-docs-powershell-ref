---
description: Disables a Configuration Manager filter rule for status messages.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Disable-CMStatusFilterRule
---

# Disable-CMStatusFilterRule

## SYNOPSIS
Disables a Configuration Manager filter rule for status messages.

## SYNTAX

### SearchByValue (Default)
```
Disable-CMStatusFilterRule -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Disable-CMStatusFilterRule -Name <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMStatusFilterRule** cmdlet disables a specified Configuration Manager filter rule for status messages.

Status filter rules specify how Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

Use the rule name and site code to specify a rule to disable.
You can use the [Enable-CMStatusFilterRule](Enable-CMStatusFilterRule.md) cmdlet to enable a rule.
To remove a rule permanently, use the [Remove-CMStatusFilterRule](Remove-CMStatusFilterRule.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Disable a status filter rule
```
PS XYZ:\>Disable-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1"
```

This command disables a status filter rule that has the specified name in a site that has the site code CM1.

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
Specifies a status filter rule object to disable.
To obtain a status filter rule object, use the [Get-CMStatusFilterRule](Get-CMStatusFilterRule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a rule.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for the Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByName
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

###  

## NOTES

## RELATED LINKS

[Enable-CMStatusFilterRule](Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](Remove-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](Set-CMStatusFilterRule.md)
