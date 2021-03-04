---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 5db024152a01fdab8233e388da5ae176849f4b7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888312"
---
# Get-AzDataFactoryPipeline

## SYNOPSIS
Obtém informações sobre pipelines no Azure Data Factory.

## SINTAXE

### ByFactoryName (Padrão)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzDataFactoryPipeline** obtém informações sobre pipelines no Azure Data Factory.
Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.
Se você não especificar um nome, esse cmdlet obterá informações sobre todos os pipelines no fábrica de dados.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os pipelines
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Este comando obtém informações sobre todos os pipelines no fábrica de dados chamado WikiADF.
Você pode um dos seguintes comandos de exemplo.
O segundo usa um **objeto DataFactory** como parâmetro.

### Exemplo 2: obter informações sobre um pipeline específico
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Este comando obtém informações sobre o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF.
O comando passa essas informações para o cmdlet Format-List usando o operador de pipeline.
Esse cmdlet formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

### Exemplo 3: Obter as propriedades de um pipeline específico
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a propriedade **Properties** associada a esse pipeline.

### Exemplo 4: Obter as atividades de um pipeline específico
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.

### Exemplo 5: Obter as informações de tempo de execução para um pipeline específico
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a **propriedade RuntimeInfo** associada a esse pipeline.

### Exemplo 6: obter informações sobre entradas para a primeira atividade
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.
O comando exibe a **propriedade Inputs** do primeiro elemento da matriz **Atividades** usando **Format-List**.

## PARÂMETROS

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet obtém pipelines que pertencem ao fábrica de dados especificado por esse parâmetro.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Especifica o nome de uma fábrica de dados.
Este cmdlet obtém pipelines que pertencem ao fábrica de dados especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Especifica o nome do pipeline sobre o qual obter informações.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Este cmdlet obtém pipelines que pertencem ao grupo especificado por esse parâmetro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## SAÍDAS

### Microsoft.Azure.Commands.DataFactories.Models.PSPipeline

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Resume-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


