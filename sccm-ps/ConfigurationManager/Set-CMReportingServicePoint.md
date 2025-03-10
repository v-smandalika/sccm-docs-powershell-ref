---
description: Modifies a Configuration Manager reporting service point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMReportingServicePoint
---

# Set-CMReportingServicePoint

## SYNOPSIS
Modifies a Configuration Manager reporting service point.

## SYNTAX

### SetByValue (Default)
```
Set-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-Force]
 -InputObject <IResultObject> [-PassThru] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-Force] [-PassThru]
 [-SiteCode <String>] [-SiteSystemServerName] <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMReportingServicePoint** cmdlet modifies a Configuration Manager reporting service point.
A reporting service point is a site system role that is installed on a server that is running Microsoft SQL Server Reporting Services.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a reporting service point
```
PS XYZ:\> Set-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4" -UserName "Contoso\DavidChew"
```

The command sets a reporting service point by using the *SiteSystemServerName* parameter.

### Example 2: Set a reporting service point by using a site system server name
```
PS XYZ:\> Set-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4" -DatabaseServerName "Contoso-TestDB.Contoso.Com" -DatabaseName "CM_CM2"
```

The command sets a reporting service point by using the *SiteSystemServerName* parameter.

### Example 3: Set a reporting service point by using an input object
```
PS XYZ:\> $RS = Get-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4"
PS XYZ:\> Set-CMReportingServicePoint -InputObject $RS -DatabaseServerName "Contoso-TestDB.Contoso.Com" -DatabaseName "CM_CM4"
```

The first command uses the **Get-CMReportingServicePoint** cmdlet to get a reporting service point, by using the *SiteSystemServerName* parameter.

The second command uses the **Set-CMReportingServicePoint** cmdlet to set the reporting point by using the input object.

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

### -DatabaseName
Specifies the name of the Configuration Manager database that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.

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

### -DatabaseServerName
Specifies the name of the Configuration Manager database server that you want to use as the data source for the reports from Microsoft SQL Server Reporting Services.
To specify a database instance, use the format \<Server Name\>\\\<Instance Name\>.

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

### -Force
Run the command without asking for confirmation.

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
Specifies an input object.
To obtain an input object, use the [Get-CMReportingServicePoint](Get-CMReportingServicePoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ReportingServicePoint

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
Specifies a site code of a Configuration Manager site that hosts this system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server hosting the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies a user name that Configuration Manager uses to connect with Microsoft SQL Server Reporting Services and that gives this user access to the site database.

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

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Add-CMReportingServicePoint](Add-CMReportingServicePoint.md)

[Get-CMReportingServicePoint](Get-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](Remove-CMReportingServicePoint.md)
