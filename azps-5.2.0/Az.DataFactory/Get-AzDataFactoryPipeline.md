---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261802"
---
# Get-AzDataFactoryPipeline

## Sinopse
Obtém informações sobre pipelines no Azure data Factory.

## SYNTAX

### ByFactoryName (padrão)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzDataFactoryPipeline** Obtém informações sobre pipelines no Azure data Factory.
Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.
Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.

## EXEMPLOS

### Exemplo 1: obter informações sobre todas as tubulações
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.
Você pode um dos comandos de exemplo a seguir.
O segundo usa um objeto **DataFactory** como parâmetro.

### Exemplo 2: obter informações sobre um pipeline específico
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.
O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.
Esse cmdlet formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

### Exemplo 3: obter as propriedades para um pipeline específico
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Properties** associada a esse pipeline.

### Exemplo 4: obter as atividades para um pipeline específico
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

Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.

### Exemplo 5: obter as informações de tempo de execução para um pipeline específico
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **RuntimeInfo** associada a esse pipeline.

### Exemplo 6: obter informações sobre as entradas para a primeira atividade
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.
O comando exibe a propriedade **inputs** do primeiro elemento da matriz **Activities** usando **Format-List**.

## OS

### -Datafactory
Especifica um objeto **PSDataFactory** .
Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.

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

### -Datafactoryname
Especifica o nome de uma fábrica de dados.
Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.

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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Nome
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
Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## EXIBE

### Microsoft. Azure. Commands. datafactorings. Models. PSPipeline

## INFORMA
* Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Currículo-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspender-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


