---
description: Calls a WMI method.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMWmiMethod
---

# Invoke-CMWmiMethod

## SYNOPSIS
Calls a WMI method.

## SYNTAX

### ByClass (Default)
```
Invoke-CMWmiMethod [-ClassName] <String> -MethodName <String> [-Parameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInstance
```
Invoke-CMWmiMethod [-InputObject] <IResultObject> -MethodName <String> [-Parameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMWmiMethod** cmdlet calls Windows Management Instrumentation (WMI) methods provided in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Call a WMI method by using the pipeline
```
PS XYZ:\> Get-CMBoundaryGroup -Name "Boundary1" | Invoke-CMWmiMethod -MethodName "AddBoundary" -Parameter @{BoundaryId = 16777217,16777218}
```

This command uses a WMI method to add an array of boundaries to a boundary group.

The command gets the boundary group object named Boundary1 and uses the pipeline operator to pass the object to **Invoke-CMWmiMethod**.
**Invoke-CMWmiMethod** calls the WMI method AddBoundary which adds the boundaries specified by their IDs to boundary group Boundary1.

## PARAMETERS

### -ClassName
Specifies the name of the WMI class that contains the static method you want to call.

```yaml
Type: String
Parameter Sets: ByClass
Aliases:

Required: True
Position: 0
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
Specifies a management object or a Configuration Management object.

```yaml
Type: IResultObject
Parameter Sets: ByInstance
Aliases: Instance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MethodName
Specifies the name of the method to invoke.
This parameter is mandatory and cannot be null or empty.

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

### -Parameter
Specifies the name of the property and the value for the method.
The name and value must be in a name/value pair.
The name/value pair is passed on the command line as a hash table.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Parameters

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

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Invoke-CMWmiQuery](Invoke-CMWmiQuery.md)


