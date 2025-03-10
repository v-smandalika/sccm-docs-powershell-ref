---
description: Configure a script installer deployment type.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Set-CMScriptDeploymentType
---

# Set-CMScriptDeploymentType

## SYNOPSIS

Configure a script installer deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMScriptDeploymentType [-ContentLocation <String>] [-AddDetectionClause <DetectionClause[]>]
 [-CacheContent <Boolean>] [-ContentFallback <Boolean>] [-DetectionClauseConnector <Hashtable[]>]
 [-EnableBranchCache <Boolean>] [-EstimatedRuntimeMins <Int32>] [-Force32Bit <Boolean>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RemoveDetectionClause <String[]>] [-RepairCommand <String>] [-RepairWorkingDirectory <String>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 -ApplicationName <String> -DeploymentTypeName <String> [-NewName <String>] [-PassThru]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMScriptDeploymentType [-ContentLocation <String>] [-AddDetectionClause <DetectionClause[]>]
 [-CacheContent <Boolean>] [-ContentFallback <Boolean>] [-DetectionClauseConnector <Hashtable[]>]
 [-EnableBranchCache <Boolean>] [-EstimatedRuntimeMins <Int32>] [-Force32Bit <Boolean>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RemoveDetectionClause <String[]>] [-RepairCommand <String>] [-RepairWorkingDirectory <String>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 -Application <IResultObject> -DeploymentTypeName <String> [-NewName <String>] [-PassThru]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMScriptDeploymentType [-ContentLocation <String>] [-AddDetectionClause <DetectionClause[]>]
 [-CacheContent <Boolean>] [-ContentFallback <Boolean>] [-DetectionClauseConnector <Hashtable[]>]
 [-EnableBranchCache <Boolean>] [-EstimatedRuntimeMins <Int32>] [-Force32Bit <Boolean>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RemoveDetectionClause <String[]>] [-RepairCommand <String>] [-RepairWorkingDirectory <String>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 -ApplicationId <Int32> -DeploymentTypeName <String> [-NewName <String>] [-PassThru]
 [-RemoveLanguage <String[]>] [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMScriptDeploymentType [-ContentLocation <String>] [-AddDetectionClause <DetectionClause[]>]
 [-CacheContent <Boolean>] [-ContentFallback <Boolean>] [-DetectionClauseConnector <Hashtable[]>]
 [-EnableBranchCache <Boolean>] [-EstimatedRuntimeMins <Int32>] [-Force32Bit <Boolean>]
 [-ForceScriptDetection32Bit <Boolean>] [-GroupDetectionClauses <String[]>]
 [-InstallationBehaviorType <InstallationBehaviorType>] [-InstallCommand <String>]
 [-InstallWorkingDirectory <String>] [-LogonRequirementType <LogonRequirementType>]
 [-MaximumRuntimeMins <Int32>] [-ProductCode <String>] [-RebootBehavior <PostExecutionBehavior>]
 [-RemoveDetectionClause <String[]>] [-RepairCommand <String>] [-RepairWorkingDirectory <String>]
 [-RequireUserInteraction <Boolean>] [-ScriptFile <String>] [-ScriptLanguage <ScriptLanguage>]
 [-ScriptText <String>] [-SlowNetworkDeploymentMode <ContentHandlingMode>] [-SourceUpdateProductCode <String>]
 [-UninstallCommand <String>] [-UninstallContentLocation <String>] [-UninstallOption <UninstallContentSetting>]
 [-UninstallWorkingDirectory <String>] [-UserInteractionMode <UserInteractionMode>] [-AddRequirement <Rule[]>]
 -InputObject <IResultObject> [-NewName <String>] [-PassThru] [-RemoveLanguage <String[]>]
 [-RemoveRequirement <Rule[]>] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the settings for a **Script Installer** deployment type of a Configuration Manager application. This deployment type can be a script or a program that installs content or does an action. You use this deployment type for setup.exe installers or script wrappers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a script installer deployment type

This command adds an uninstall command to the deployment type named **ScriptDT01** for the application named **Application01**.

```powershell
Set-CMScriptDeploymentType -ApplicationName "Application01" -DeploymentTypeName "ScriptDT01" -Comment "Script updated to uninstall" -UninstallCommand 'msiexec /x ""\\Machine01\Resources\Applications\MSI\AdvertMSI\AdvertMSI.msi" /q'
```

### Example 2: Add a detection method

This example first uses the **New-CMDetectionClauseFile** cmdlet to create three file-based detection clauses for the file c:\abc\abc with a size of 1 KB, 2 KB, and 4 KB.

It then configures the deployment type to add these clauses as a detection method. It also groups the second and third clause with an **OR** connector.

```powershell
$clauseFile1 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 1024 -ExpressionOperator IsEquals -Value
$clauseFile2 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 2048 -ExpressionOperator IsEquals -Value
$clauseFile3 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 4096 -ExpressionOperator IsEquals -Value

Set-CMScriptDeploymentType -ApplicationName "testApp1" -DeploymentTypeName "abc" -AddDetectionClause $clauseFile1,$clauseFile2,$clauseFile3 -DetectionClauseConnector @{"LogicalName"=$clauseFile3.Setting.LogicalName;"Connector"="OR"} -GroupDetectionClauses $clauseFile2.Setting.LogicalName, $clauseFile3.Setting.LogicalName
```

### Example 3: Add a language requirement rule

This example configures the app with a requirement rule for the OS languge.

```powershell
$myGC = Get-CMGlobalCondition -Name "Operating System Language" | Where-Object PlatformType -eq 1
$cultureA = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "zh"
$cultureB = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "zh-CN"
$myRule = $myGC | New-CMRequirementRuleOperatingSystemLanguageValue -RuleOperator NoneOf -Culture $cultureA,$cultureB -IsMobile $False

Set-CMScriptDeploymentType -ApplicationName "myApp" -DeploymentTypeName "myDT" -AddRequirement $myRule
```

### Example 4: Add a requirement rule

This example configures the app with a requirement rule that physical memory is greater than 2 GB.

```powershell
$rule1 = Get-CMGlobalCondition -Name "Total physical memory" | New-CMRequirementRuleCommonValue -Value1 2048 -RuleOperator GreaterEquals
$myRuleExpression = New-CMRequirementRuleExpression -AddRequirementRule $rule1
$myGC = New-CMGlobalConditionExpression -Name "GCExp" -DeviceType Windows -RootExpression $myRuleExpression

Set-CMScriptDeploymentType -ApplicationName "myApp" -DeploymentTypeName "myDT" -AddRequirement $myGC
```

## PARAMETERS

### -AddDetectionClause

Specify an array of detection method clauses for this deployment type. To create a detection clause, use one of the following cmdlets:

- [New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)
- [New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)
- [New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)
- [New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)
- [New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)

Save the output of these cmdlets into a variable. Then specify those variables as an array for this parameter. For example, `-AddDetectionClause $clauseFile1,$clauseFile2,$clauseFile3`.

```yaml
Type: DetectionClause[]
Parameter Sets: (All)
Aliases: AddDetectionClauses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguage

Specify an array of language tags that the deployment type supports. For example, to add **Russian (Russia)**, specify the tag `ru-RU`.

For more information and a list of language tags, see [Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguages, Languages, Language

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequirement

Specify an array of requirement objects for the deployment type. To create a requirement rule object, use one of the following cmdlets:

- [New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
- [New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
- [New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
- [New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
- [New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
- [New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
- [New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
- [New-CMRequirementRuleFileAttributeValue](New-CMRequirementRuleFileAttributeValue.md)
- [New-CMRequirementRuleFilePermissionValue](New-CMRequirementRuleFilePermissionValue.md)
- [New-CMRequirementRuleFreeDiskSpaceValue](New-CMRequirementRuleFreeDiskSpaceValue.md)
- [New-CMRequirementRuleInputTypeValue](New-CMRequirementRuleInputTypeValue.md)
- [New-CMRequirementRuleOperatingSystemLanguageValue](New-CMRequirementRuleOperatingSystemLanguageValue.md)
- [New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
- [New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
- [New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
- [New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Application

Specify an application object for this deployment type. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByAppValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Specify the ID of the application for this deployment type.

```yaml
Type: Int32
Parameter Sets: ByAppId
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specify the name of the application for this deployment type.

```yaml
Type: String
Parameter Sets: ByAppName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CacheContent

Set this parameter to `$true` to save content indefinitely in the client cache.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PersistContentInClientCache

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specify an optional description for the deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdministratorComment

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

### -ContentFallback

If you set this parameter to `$true`, when the content isn't available on any distribution points in the client's current or neighbor boundary groups, the client can use distribution points in the site default boundary group.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableContentLocationFallback, AllowClientsToUseFallbackSourceLocationForContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentLocation

Specifies the network source path of the content. The site system server requires permission to read the content files.

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

### -DeploymentTypeName

Specify the name of the deployment type to configure.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppValue, ByAppId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetectionClauseConnector

When you use the **GroupDetectionClauses** parameter to group detection clauses, use this parameter to specify the connector.

The following example defines the **OR** connector: `@{"LogicalName"=$clauseFile3.Setting.LogicalName;"Connector"="OR"}`

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: DetectionClauseConnectors

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

### -EnableBranchCache

This parameter is deprecated. BranchCache is always enabled on clients, and they use it if the distribution point supports it.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowClientsToShareContentOnSameSubnet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EstimatedRuntimeMins

Specify the estimated installation time, in minutes, of this deployment type for the application. Software Center displays this estimate to the user before the application installs.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: EstimatedInstallationTimeMinutes, EstimatedInstallationTimeMins, EstimatedRunTimeMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ForceForUnknownPublisher

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force32Bit

Set this parameter to `$true` to run the install and uninstall programs as 32-bit processes on 64-bit clients.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Force32BitInstaller

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceScriptDetection32Bit

If you use a custom script to detect the presence of this deployment type, set this parameter to `$true` to run the script as a 32-bit process on 64-bit clients.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Force32BitDetectionScript

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

### -GroupDetectionClauses

When you configure rules to detect the presence of this deployment type, use this parameter to group clauses. To create a detection clause, use one of the following cmdlets:

- [New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)
- [New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)
- [New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)
- [New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)
- [New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)

Save the output of these cmdlets into a variable. Then use the following format to group clauses: `$clause2.Setting.LogicalName, $clause3.Setting.LogicalName`.

> [!TIP]
> In the Configuration Manager console, when you select the **Group** action, the clauses show parentheses before and after the grouped clauses.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: GroupDetectionClausesByLogicalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a deployment type object to configure. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByDTValue
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallCommand

Specify the installation program command line to install this application.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallWorkingDirectory

Specify the path to use as the working directory when the client runs the **InstallCommand**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationStartIn, InstallFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationBehaviorType

Specify the installation behavior for this deployment type:

- `InstallForUser`: The client only installs the application for the user to whom you deploy the application.
- `InstallForSystem`: The client installs the application only once. It's available to all users.
- `InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser`: If you deploy the application to a device, the client installs it for all users. If you deploy the application to a user, the client only installs it for that user.

```yaml
Type: InstallationBehaviorType
Parameter Sets: (All)
Aliases:
Accepted values: InstallForUser, InstallForSystem, InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogonRequirementType

Specify the requirement for a signed-in user:

- `OnlyWhenNoUserLoggedOn`: Only when no user is signed into Windows.
- `OnlyWhenUserLoggedOn`: Only when a user is signed in. This option is the default.
- `WhetherOrNotUserLoggedOn`: Whether or not a user is signed in.

    > [!NOTE]
    > The value `WhereOrNotUserLoggedOn` is deprecated. It's replaced by `WhetherOrNotUserLoggedOn`.

If you set **InstallationBehaviorType** to `InstallForUser`, then you can't set this parameter.

```yaml
Type: LogonRequirementType
Parameter Sets: (All)
Aliases:
Accepted values: OnlyWhenUserLoggedOn, WhereOrNotUserLoggedOn, WhetherOrNotUserLoggedOn, OnlyWhenNoUserLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumRuntimeMins

Specify the maximum allowed run time of the deployment program for this application. Set an integer value in minutes.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumAllowedRunTimeMinutes, MaximumAllowedRunTimeMins, MaximumRunTimeMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name to rename this deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewDeploymentTypeName

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

### -ProductCode

If the application uses Windows Installer technology, specify an MSI product code to set as the detection method. When you use this parameter, it overwrites any existing detection methods.

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

### -RebootBehavior

Specify the post-installation behavior:

- `BasedOnExitCode`: Determine behavior based on return codes.

- `NoAction`: No specific action.

- `ProgramReboot`: The software install program might force a device restart.

- `ForceReboot`: Configuration Manager client will force a mandatory device restart.

For more information on these behaviors, see [Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications#deployment-type-properties-user-experience-options).

```yaml
Type: PostExecutionBehavior
Parameter Sets: (All)
Aliases:
Accepted values: BasedOnExitCode, NoAction, ForceReboot, ProgramReboot

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveDetectionClause

Specify an array of detection method clauses to remove.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveDetectionClauses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguage

Specify an array of supported languages to remove from this deployment type.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRequirement

Specify an array of requirement rules to remove from this deployment type.

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases: RemoveRequirements

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RepairCommand

Starting in version 2002, use this parameter to configure the repair command. Also configure the **RepairWorkingDirectory** parameter.

Starting in version 2006, you can specify an empty string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RepairProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RepairWorkingDirectory

Starting in version 2002, use this parameter to configure the repair command's working directory. Also configure the **RepairCommand** parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RepairStartIn, RepairFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireUserInteraction

Set this parameter to `$true` to allow users to view and interact with the deployment type installation.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RequiresUserInteraction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptFile

Specify the script file to use to detect this deployment type. Also use the **ScriptLanguage** parameter.

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

### -ScriptLanguage

If you use the **ScriptFile** or **ScriptText** parameters, use this parameter to specify the script language.

```yaml
Type: ScriptLanguage
Parameter Sets: (All)
Aliases: ScriptType
Accepted values: PowerShell, VBScript, JavaScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptText

Specify the text of a script to detect this deployment type. Also use the **ScriptLanguage** parameter.

For more information, see [About custom script detection methods](/mem/configmgr/apps/deploy-use/create-applications#about-custom-script-detection-methods).

```yaml
Type: String
Parameter Sets: (All)
Aliases: ScriptContent, Script

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowNetworkDeploymentMode

When a client uses a distribution point from a neighbor boundary group or the default site boundary group, specify the deployment option:

- `DoNothing`: Don't download content
- `Download`: Download content from the distribution point and run locally

```yaml
Type: ContentHandlingMode
Parameter Sets: (All)
Aliases:
Accepted values: DoNothing, Download

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceUpdateProductCode

If the application uses Windows Installer technology, specify an MSI product code. This product code is a GUID format.

Windows Source management enables an .MSI represented by this deployment type to automatically be updated or repaired from content source files on an available distribution point.

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

### -UninstallCommand

Specifies the command line to uninstall the application.

Starting in version 2006, you can specify an empty string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UninstallationProgram

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallContentLocation

Specify the network path to source content to use with the **UninstallCommand** that's different from the **ContentLocation**. Use this parameter when you set **UninstallOption** to `Different`.

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

### -UninstallOption

Specify what content to use with the **UninstallCommand**:

- `SameAsInstall`: The install and uninstall content are the same. This option is the default.
- `NoneRequired`: The application doesn't need content for uninstall.
- `Different`: The uninstall content is different from the install content. Use **UninstallContentLocation** to specify the network path to the content that's used to uninstall the application.

```yaml
Type: UninstallContentSetting
Parameter Sets: (All)
Aliases:
Accepted values: SameAsInstall, NoneRequired, Different

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UninstallWorkingDirectory

Specify the path to use as the working directory when the client runs the **UninstallCommand**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UninstallationStartIn, UninstallFolder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserInteractionMode

Specify the installation program visibility:

- `Normal`: The deployment type runs in the normal mode based on system and program defaults. This mode is the default.
- `Minimized`: The deployment type runs minimized on client devices. Users might see the installation activity in the notification area or taskbar.
- `Maximized`: The deployment type runs maximized on client devices. Users see all installation activity.
- `Hidden`: The deployment type runs hidden on client devices. Users see no installation activity.

```yaml
Type: UserInteractionMode
Parameter Sets: (All)
Aliases: InstallationProgramVisibility
Accepted values: Normal, Minimized, Maximized, Hidden

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

[Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)

[Get-CMApplication](Get-CMApplication.md)

[Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications)
