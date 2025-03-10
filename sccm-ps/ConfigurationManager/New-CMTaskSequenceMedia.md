---
description: Creates task sequence media in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2018
schema: 2.0.0
title: New-CMTaskSequenceMedia
---

# New-CMTaskSequenceMedia

## SYNOPSIS

Creates task sequence media in Configuration Manager.

## SYNTAX

### NewBootableMedia (Default)
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>] [-BootableMedia]
 -BootImageDistributionPointServerName <String> -BootImageId <String>
 -BootImageManagementPointServerName <String[]> [-CommandDistributionPointServerName <String>]
 [-CommandIncludeFile <Boolean>] [-CommandPackageName <String>] [-CreateMediaSelfCertificate <Boolean>]
 [-DriveName <String>] [-EnablePrestartCommand <Boolean>] [-EnableUnknownSupport <Boolean>]
 [-ExpirationDate <DateTime>] [-ImportCertificatePassword <SecureString>] [-ImportCertificatePath <String>]
 -MediaInputType <MediaInputType> -MediaMode <MediaMode> -MediaPath <String> [-MediaSize <MediaSize>]
 [-Password <SecureString>] [-PrestartCommandLine <String>] -ProtectPassword <Boolean> [-StartDate <DateTime>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewStandAloneMedia
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>]
 [-CommandDistributionPointServerName <String>] [-CommandIncludeFile <Boolean>] [-CommandPackageName <String>]
 [-DriveName <String>] [-EnablePrestartCommand <Boolean>] [-IncludeApplicationDependency <Boolean>]
 -MediaInputType <MediaInputType> -MediaPath <String> [-MediaSize <MediaSize>] [-Password <SecureString>]
 [-PrestartCommandLine <String>] -ProtectPassword <Boolean> [-StandaloneMedia]
 -TaskSequenceDistributionPointServerName <String[]> -TaskSequenceId <String> [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewStandAloneMediaByValue
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>]
 [-CommandIncludeFile <Boolean>] [-CommandPackage <IResultObject>]
 [-CommandPackageDistributionPoint <IResultObject>] [-DriveName <String>] [-EnablePrestartCommand <Boolean>]
 [-IncludeApplicationDependency <Boolean>] [-MediaInputType <MediaInputType>] -MediaPath <String>
 [-MediaSize <MediaSize>] [-Password <SecureString>] [-PrestartCommandLine <String>]
 [-ProtectPassword <Boolean>] [-StandaloneMedia] -TaskSequence <IResultObject>
 -TaskSequenceDistributionPoint <IResultObject[]> [-Variable <Hashtable>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewBootableMediaByValue
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>] [-BootableMedia]
 -BootImage <IResultObject> -BootImageDistributionPoint <IResultObject>
 -BootImageManagementPoint <IResultObject[]> [-CommandIncludeFile <Boolean>] [-CommandPackage <IResultObject>]
 [-CommandPackageDistributionPoint <IResultObject>] [-CreateMediaSelfCertificate <Boolean>]
 [-DriveName <String>] [-EnablePrestartCommand <Boolean>] [-EnableUnknownSupport <Boolean>]
 [-ExpirationDate <DateTime>] [-ImportCertificatePassword <SecureString>] [-ImportCertificatePath <String>]
 [-MediaInputType <MediaInputType>] [-MediaMode <MediaMode>] -MediaPath <String> [-MediaSize <MediaSize>]
 [-Password <SecureString>] [-PrestartCommandLine <String>] [-ProtectPassword <Boolean>]
 [-StartDate <DateTime>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewPrestagedMedia
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>]
 [-Application <IResultObject[]>] [-ApplicationName <String[]>] -BootImageDistributionPointServerName <String>
 -BootImageId <String> -BootImageManagementPointServerName <String[]>
 [-CommandDistributionPointServerName <String>] [-CommandIncludeFile <Boolean>] [-CommandPackageName <String>]
 [-Comment <String>] [-CreatedBy <String>] [-DriverPackage <IResultObject[]>] [-DriverPackageName <String[]>]
 -MediaMode <MediaMode> -MediaPath <String> -OperatingSystemImageDistributionPointServerName <String>
 [-OperatingSystemImageName <String>] [-OperatingSystemImagePackageId <String>] [-Package <IResultObject[]>]
 [-PackageName <String[]>] [-PrestagedMedia] [-PrestartCommandLine <String>] -ProtectPassword <Boolean>
 -TaskSequenceDistributionPointServerName <String[]> -TaskSequenceId <String> [-Variable <Hashtable>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewPrestagedMediaByValue
```
New-CMTaskSequenceMedia [-AllowUacPrompt] [-AllowUnattendedDeployment <Boolean>]
 [-Application <IResultObject[]>] -BootImage <IResultObject> -BootImageDistributionPoint <IResultObject>
 -BootImageManagementPoint <IResultObject[]> [-CommandIncludeFile <Boolean>] [-CommandPackage <IResultObject>]
 [-CommandPackageDistributionPoint <IResultObject>] [-Comment <String>] [-CreatedBy <String>]
 [-DriverPackage <IResultObject[]>] -MediaMode <MediaMode> -MediaPath <String>
 -OperatingSystemImageDistributionPoint <IResultObject> [-OperatingSystemImagePackage <IResultObject>]
 [-Package <IResultObject[]>] [-PrestagedMedia] [-PrestartCommandLine <String>] [-ProtectPassword <Boolean>]
 -TaskSequence <IResultObject> -TaskSequenceDistributionPoint <IResultObject[]> [-Variable <Hashtable>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewCaptureMediaByValue
```
New-CMTaskSequenceMedia [-AllowUacPrompt] -BootImage <IResultObject>
 -BootImageDistributionPoint <IResultObject> [-CaptureMedia] [-DriveName <String>]
 [-MediaInputType <MediaInputType>] -MediaPath <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewCaptureMedia
```
New-CMTaskSequenceMedia [-AllowUacPrompt] -BootImageDistributionPointServerName <String> -BootImageId <String>
 [-CaptureMedia] [-DriveName <String>] -MediaInputType <MediaInputType> -MediaPath <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTaskSequenceMedia** cmdlet creates task sequence media in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create task sequence media with the captured media option

```powershell
PS XYZ:\> New-CMTaskSequenceMedia -CaptureMediaOption -MediaPath "\\Contoso320\Users\Administrator.Contoso319DOM\Desktop\DD\1.iso" -MediaInputType CDDVD -BootImageName "Boot" -DistributionPointServerName "Contoso320.Contoso319DOM.NET"
```

This command creates task sequence media by specifying the *CaptureMediaOption* parameter.
The command also specifies a value for the *MediaPath* parameter, and a value for the *MediaInputType* parameter.

### Example 2: Create task sequence media with the standalone media option

```powershell
PS XYZ:\> $Group = @{"6"="8";}
PS XYZ:\> New-CMTaskSequenceMedia -StandAloneMediaOption -Variable $Group -MediaInputType CDDVD -MediaPath "\\Contoso320\Users\Administrator.Contoso319DOM\Desktop\DD\111 - Copy.iso" -ProtectPassword 0 -TaskSequenceId "CCC0000B" -TaskSequenceDistributionPointServerName "\\Contoso320.Contoso319DOM.NET"
```

The first command creates a mapping, and then stores the result in the $Group variable.

The second command creates task sequence media by specifying the *StandAloneMediaOption* parameter.

### Example 3: Create task sequence media with the bootable media option

```powershell
PS XYZ:\> New-CMTaskSequenceMedia -BootableMediaOption -MediaInputType CDDVD -MediaPath "\\Contoso320\Users\Administrator.Contoso319DOM\Desktop\DD\111 - Copy (6).iso" -MediaMode Dynamic -ProtectPassword 0 -BootImageName "boot" -DistributionPointServerName "Contoso320.Contoso319DOM.NET" -ManagementnPointNetworkOperatingSystemPath "Contoso320.Contoso319DOM.NET"
```

This command creates task sequence media by specifying the *BootableMediaOption* parameter.

### Example 4: Create task sequence media with the prestaged media option

```powershell
PS XYZ:\> New-CMTaskSequenceMedia -PrestagedMediaOption -MediaMode Dynamic -MediaPath "\\Contoso320\Users\Administrator.Contoso319DOM\Desktop\DD\2.wim"  -ProtectPassword 0 -TaskSequenceId "CCC0000B" -BootImageName "boot" -DistributionPointServerName "Contoso320.Contoso319DOM.NET" -ManagementnPointNetworkOperatingSystemPath "Contoso320.Contoso319DOM.NET" -OperatingSystemImageDistributionPointServerName "Contoso320.Contoso319DOM.NET" -TaskSequenceDistributionPointServerName "\\Contoso320.Contoso319DOM.NET"
```

This command uses the **New-CMTaskSequenceMedia** cmdlet to create task sequence media by specifying the *PrestagedMediaOption* parameter.

## PARAMETERS

### -AllowUacPrompt

Indicates that User Account Control (UAC) prompts are allowed.

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

### -AllowUnattendedDeployment

Indicates whether you allow unattended operating system deployment, which does not prompt for network configuration or optional task sequences.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMedia, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Application

Specifies applications included in the task sequence.

```yaml
Type: IResultObject[]
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
Aliases: Applications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationName

Specifies an array of names of applications included in the task sequence.

```yaml
Type: String[]
Parameter Sets: NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImage

Specifies a boot image object.

```yaml
Type: IResultObject
Parameter Sets: NewBootableMediaByValue, NewPrestagedMediaByValue, NewCaptureMediaByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BootImageDistributionPoint

Specifies a boot image distribution point.

```yaml
Type: IResultObject
Parameter Sets: NewBootableMediaByValue, NewPrestagedMediaByValue, NewCaptureMediaByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BootImageDistributionPointServerName

Specifies a boot image distribution point server name.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewPrestagedMedia, NewCaptureMedia
Aliases: DistributionPointServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId

Specifies the ID of the boot image package associated with the task sequence media.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewPrestagedMedia, NewCaptureMedia
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageManagementPoint

Specifies a boot image management point.

```yaml
Type: IResultObject[]
Parameter Sets: NewBootableMediaByValue, NewPrestagedMediaByValue
Aliases: BootImageManagementPoints

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BootImageManagementPointServerName

Specifies a boot image management point server name.

```yaml
Type: String[]
Parameter Sets: NewBootableMedia, NewPrestagedMedia
Aliases: ManagementPointServerName, BootImageManagementPointServerNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootableMedia

```yaml
Type: SwitchParameter
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases: BootableMediaOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureMedia

```yaml
Type: SwitchParameter
Parameter Sets: NewCaptureMediaByValue, NewCaptureMedia
Aliases: CaptureMediaOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandDistributionPointServerName

Specifies a name for a distribution point server from which the cmdlet acquires the package.
The *CommandPackageName* parameter specifies the package name.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandIncludeFile

Indicates whether to include a file.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMedia, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandPackage

Specifies a command package.

```yaml
Type: IResultObject
Parameter Sets: NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandPackageDistributionPoint

Specifies a command package distrubtion point.

```yaml
Type: IResultObject
Parameter Sets: NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandPackageName

Specifies a package name for the command specified by the *CommandLine* parameter.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specifies a comment for a prestaged media file.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
Aliases:

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

### -CreateMediaSelfCertificate

Indicates whether the media includes a self-signed certificate.
Use this parameter only in mixed-mode environments.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreatedBy

Specifies the name of an individual or organization responsible for the creation of the prestaged media.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
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

### -DriveName

Specifies a drive name.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue, NewCaptureMediaByValue, NewCaptureMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackage

Specifies a driver package.

```yaml
Type: IResultObject[]
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
Aliases: DriverPackages, PackageDriver, PackageDrivers

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DriverPackageName

Specifies the name of a driver package.

```yaml
Type: String[]
Parameter Sets: NewPrestagedMedia
Aliases: PackageDriverName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePrestartCommand

Indicates whether to enable a prestart command.
A prestart command is a script or executable that runs before the task sequence.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUnknownSupport

Indicates whether to provision unknown systems for operating system deployment.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpirationDate

Specifies an expiration date, in D.HH:MM:SS format, for bootable media.

```yaml
Type: DateTime
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
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

### -ImportCertificatePassword

Specifies a password for an import certificate, as a secure string.
An import certificate is a PKI-issued certificate added to the boot media for client authentication and communication with a Configuration Manager site.

```yaml
Type: SecureString
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportCertificatePath

Specifies a path for an import certificate to add to the boot media.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeApplicationDependency

Indicates that the cmdlet detects associated application dependencies and adds them to this media.

```yaml
Type: Boolean
Parameter Sets: NewStandAloneMedia, NewStandAloneMediaByValue
Aliases: IncludeApplicationDependencies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaInputType

Specifies a media input type.
The acceptable values for this parameter are:

- CDDVD
- USB

```yaml
Type: MediaInputType
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewCaptureMedia
Aliases:
Accepted values: Usb, CdDvd, Hd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: MediaInputType
Parameter Sets: NewStandAloneMediaByValue, NewBootableMediaByValue, NewCaptureMediaByValue
Aliases:
Accepted values: Usb, CdDvd, Hd

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaMode

Specifies a media mode.
The acceptable values for this parameter are:

- Dynamic
- SiteBased

```yaml
Type: MediaMode
Parameter Sets: NewBootableMedia, NewPrestagedMedia, NewPrestagedMediaByValue
Aliases:
Accepted values: Dynamic, SiteBased

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: MediaMode
Parameter Sets: NewBootableMediaByValue
Aliases:
Accepted values: Dynamic, SiteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaPath

Specifies a path to the media.

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

### -MediaSize

Specifies the size of the media.
The acceptable values for this parameter are:

- None
- Size4GB
- Size650MB
- Size8GB
- SizeUnlimited

```yaml
Type: MediaSize
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue
Aliases:
Accepted values: None, Size650MB, Size4GB, Size8GB, SizeUnlimited

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageDistributionPoint

```yaml
Type: IResultObject
Parameter Sets: NewPrestagedMediaByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperatingSystemImageDistributionPointServerName

Specifies the name of a distribution point server for an operating system image.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageName

Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImagePackage

```yaml
Type: IResultObject
Parameter Sets: NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperatingSystemImagePackageId

Specifies the identifier of an operating system image package.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package

Specifies package objects.

```yaml
Type: IResultObject[]
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
Aliases: Packages

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageName

Specifies an array of package names.

```yaml
Type: String[]
Parameter Sets: NewPrestagedMedia
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password

Specifies a password, as a secure string.

```yaml
Type: SecureString
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestagedMedia

```yaml
Type: SwitchParameter
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
Aliases: PrestagedMediaOption, PrestageMedia

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartCommandLine

Specifies a pre-start command line.

```yaml
Type: String
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMedia, NewPrestagedMediaByValue
Aliases: CommandLine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectPassword

Indicates whether to protect the media with a password.

```yaml
Type: Boolean
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewPrestagedMedia
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Boolean
Parameter Sets: NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandaloneMedia

```yaml
Type: SwitchParameter
Parameter Sets: NewStandAloneMedia, NewStandAloneMediaByValue
Aliases: StandAloneMediaOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate

Specifies a start date and time, in D.HH:MM:SS format.

```yaml
Type: DateTime
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequence

Specifies a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: NewStandAloneMediaByValue, NewPrestagedMediaByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceDistributionPoint

Specifies a task sequence distribution point.

```yaml
Type: IResultObject[]
Parameter Sets: NewStandAloneMediaByValue, NewPrestagedMediaByValue
Aliases: TaskSequenceDistributionPoints

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceDistributionPointServerName

Specifies an array of available distribution point servers for a task sequence.

```yaml
Type: String[]
Parameter Sets: NewStandAloneMedia, NewPrestagedMedia
Aliases: TaskSequenceDistributionPointServerNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId

Specifies an ID for a task sequence.

```yaml
Type: String
Parameter Sets: NewStandAloneMedia, NewPrestagedMedia
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeviceAffinity

Specifies user device affinity.
User device affinity associates users with a destination computer.
The acceptable values for this parameter are:

- AdministratorApproval
- AutoApproval
- DoNotAllow

```yaml
Type: UserDeviceAffinityType
Parameter Sets: NewBootableMedia, NewBootableMediaByValue
Aliases:
Accepted values: DoNotAllow, AdministratorApproval, AutoApproval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable

Specifies a task sequence variable.
The task sequence variable consists of a name and a value.

```yaml
Type: Hashtable
Parameter Sets: NewBootableMedia, NewStandAloneMedia, NewStandAloneMediaByValue, NewBootableMediaByValue, NewPrestagedMedia, NewPrestagedMediaByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version

Specifies the version information for the media.

```yaml
Type: String
Parameter Sets: NewPrestagedMedia, NewPrestagedMediaByValue
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

###  

## NOTES

## RELATED LINKS

[Get-CMTaskSequence](Get-CMTaskSequence.md)
