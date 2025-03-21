﻿---
external help file: AdminUI.PS-help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2020
online version:
schema: 2.0.0
---

# Get-CMCollectionInfoFromFullEvaluationQueue

## SYNOPSIS

Get collection information from the full evaluation queue.

## SYNTAX

### ByName (Default)
```
Get-CMCollectionInfoFromFullEvaluationQueue [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMCollectionInfoFromFullEvaluationQueue -Id <String> [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionInfoFromFullEvaluationQueue -InputObject <IResultObject> [<CommonParameters>]
```

## DESCRIPTION

Get collection information from the full evaluation queue. For more information, see [How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view).

> [!TIP]
> The collection evaluation process happens on primary sites, not on the central administration site (CAS). Use this cmdlet when connected to a primary site.

## EXAMPLES

### Example 1

```powershell
Get-CMCollectionInfoFromFullEvaluationQueue -Id "SMS00002"
```

## PARAMETERS

### -Id

Specify the ID of a collection to query. For example, `"SMS00002"`.

```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a collection object to query. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of a collection to query. For example, `"All Users"`.

```yaml
Type: String
Parameter Sets: ByName
Aliases: CollectionName

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

[Get-CMCollectionEvaluationStatus](Get-CMCollectionEvaluationStatus.md)

[Get-CMCollectionFullEvaluationStatus](Get-CMCollectionFullEvaluationStatus.md)

[Get-CMCollectionIncrementalEvaluationStatus](Get-CMCollectionIncrementalEvaluationStatus.md)

[Get-CMCollectionInfoFromEvaluationQueue](Get-CMCollectionInfoFromEvaluationQueue.md)

[Get-CMCollectionInfoFromIncrementalEvaluationQueue](Get-CMCollectionInfoFromIncrementalEvaluationQueue.md)

[Get-CMCollectionInfoFromManualEvaluationQueue](Get-CMCollectionInfoFromManualEvaluationQueue.md)

[Get-CMCollectionInfoFromNewEvaluationQueue](Get-CMCollectionInfoFromNewEvaluationQueue.md)

[How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view)

[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
