---
description: Changes the settings of an Application Catalog website point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMApplicationCatalogWebsitePoint
---

# Set-CMApplicationCatalogWebsitePoint

## SYNOPSIS
Changes the settings of an Application Catalog website point.

## SYNTAX

### SetByValue (Default)
```
Set-CMApplicationCatalogWebsitePoint [-ApplicationWebServicePointServerName <String>]
 [-ClientConnectionType <ClientConnectionTypes>] [-Color <Color>] [-ColorBlue <Int32>] [-ColorGreen <Int32>]
 [-ColorRed <Int32>] [-CommunicationType <ComputerCommunicationType>] -InputObject <IResultObject>
 [-NetBiosName <String>] [-OrganizationName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMApplicationCatalogWebsitePoint [-ApplicationWebServicePointServerName <String>]
 [-ClientConnectionType <ClientConnectionTypes>] [-Color <Color>] [-ColorBlue <Int32>] [-ColorGreen <Int32>]
 [-ColorRed <Int32>] [-CommunicationType <ComputerCommunicationType>] [-NetBiosName <String>]
 [-OrganizationName <String>] [-PassThru] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMApplicationCatalogWebsitePoint** cmdlet changes the settings of an Application Catalog website point in Configuration Manager.
This site system role supports the Application Catalog website.

Specify the site that this website point supports and the server that hosts the website point.
You can specify the website name and NetBIOS name of the Application Catalog.

You can customize the page that users see when they connect to the Application Catalog.
Specify custom values for the colors blue, green, and red.
You can also specify a name for users to see in the browser, such as a company name or a division within a company.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the settings of an Application Catalog website point
```
PS XYZ:\> Set-CMApplicationCatalogWebsitePoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM" -SiteCode "CM4" -NetbiosName "CMDIV-WEST02" -OrganizationName "MarketingWest" -ColorRed 168 -ColorGreen 201 -ColorBlue 52
```

This command changes the settings of the Application Catalog website point hosted on the site system server named CMDIV-WEST04.CORP.CONTOSO.COM.
The command specifies that the NetBIOS server named CMDIV-WEST02 hosts the Application Catalog website point.
The command specifies that Configuration Manager displays the organization name MarketingWest in the Software Center, and sets the custom colors for the Software Center.

### Example 2: Change the settings of an Application Catalog website point by object variable
```
PS XYZ:\> $Acwp= Get-CMApplicationCatalogWebsitePoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM" -SiteCode "CM4"
PS XYZ:\> Set-CMApplicationCatalogWebsitePoint -InputObject $Acwp -NetbiosName "CMDIV-WEST02" -OrganizationName "MarketingWest" -ColorR 160 -ColorG 200 -ColorB 50
```

The first command uses the Get-CMApplicationCatalogWebsitePoint cmdlet to get the Application Catalog website point that is associated with the site system server named CMDIV-WEST04.CORP.CONTOSO.COM that is hosted on the Configuration Manager site that has the site code CM4.
The command stores the result in the $Acwp variable.

The second command changes the settings of the Application Catalog website point stored in $Acwp.
The command specifies that the NetBIOS server named CMDIV-WEST02 hosts the Application Catalog website point.
The command specifies that Configuration Manager displays the organization name MarketingWest in the Software Center, and sets the custom colors for the Software Center.

## PARAMETERS

### -ApplicationWebServicePointServerName
```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteSystemServerNameConfiguredForApplicationCatalogWebServicePoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientConnectionType
Specifies the client connection type.
The acceptable values for this parameter are:

-  Internet
- InternetAndIntranet
- Intranet

```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases:
Accepted values: Intranet, Internet, InternetAndIntranet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Color
```yaml
Type: Color
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorBlue
Specifies an integer value for a custom blue color.
Configuration Manager uses custom colors to conform to customer branding.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorGreen
Specifies an integer value for a custom green color.
Configuration Manager uses custom colors to conform to customer branding.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorRed
Specifies an integer value for a custom red color.
Configuration Manager uses custom colors to conform to customer branding.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommunicationType
```yaml
Type: ComputerCommunicationType
Parameter Sets: (All)
Aliases: ClientCommunicationType
Accepted values: Http, Https

Required: False
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
Specifies an Application Catalog website point object.
To obtain Application Catalog website point object, use the Get-CMApplicationCatalogWebsitePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ApplicationCatalogWebsitePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NetBiosName
Specifies the NetBIOS name of the server that hosts the Application Catalog website point.

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

### -OrganizationName
Specifies a name for a customer organization.
This name appears to users who access the Application Catalog.

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
Specifies the site code for a Configuration Manager site.

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
Specifies the name of a server that hosts a site system role.

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

[Add-CMApplicationCatalogWebsitePoint](Add-CMApplicationCatalogWebsitePoint.md)

[Get-CMApplicationCatalogWebServicePoint](Get-CMApplicationCatalogWebServicePoint.md)

[Get-CMApplicationCatalogWebsitePoint](Get-CMApplicationCatalogWebsitePoint.md)

[Remove-CMApplicationCatalogWebSitePoint](Remove-CMApplicationCatalogWebSitePoint.md)
