---
description: Modifies general settings for a Configuration Manager global condition.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: Set-CMGlobalConditionGeneral
---

# Set-CMGlobalConditionGeneral

## SYNOPSIS

Modifies general settings for a Configuration Manager global condition.

## SYNTAX

```
Set-CMGlobalConditionGeneral [-Description <String>] [-NewName <String>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMGlobalConditionGeneral** cmdlet modifies general settings for a global condition.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Set-CMGlobalConditionGeneral -Name newscript -NewName newscript2 -Description Description2
```

This command modifies the name and the description.

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description.

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

### -Name

Specifies a name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specifies a new name.

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

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalCondition](./Set-CMGlobalCondition.md)

[Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)

[Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)

[Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)

[Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)

[Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)

[Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)

[Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)

[Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)

[Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)

[Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)

[Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)
