---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118810"
---
# Set-AzDataFactorySliceStatus

## Sinopse
Define o status das fatias para um conjunto de dados no Azure Data Factory.

## Sintaxe

### ByFactoryName (Default)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzDataFactorySliceStatus** define o status das fatias de um conjunto de dados no Azure Data Factory.

## Exemplos

### Exemplo 1: Definir o status de todas as fatias
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Esse comando define o status de todas as fatias para o conjunto de dados chamado DAWikiAggregatedData como Aguardando na fábrica de dados chamada WikiADF.
O *parâmetro UpdateType* tem um valor de UpstreamInStreamLine e, portanto, o comando define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes.
Os conjuntos de dados dependentes são usados como conjuntos de dados de entrada para atividades no pipeline.
Esse comando retorna um valor de $True.

## Parâmetros

### -DataFactory
Especifica um **objeto PSDataFactory.**
Esse cmdlet modifica o status das fatias que pertencem à fábrica de dados especificada por esse parâmetro.

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
Esse cmdlet modifica o status das fatias que pertencem à fábrica de dados especificada por esse parâmetro.

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

### -NomedoConjunto de Dados
Especifica o nome do conjuntos de dados para o qual este cmdlet modifica as fatias.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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

### -EndDateTime
Especifica o fim de um período de tempo como um **objeto DateTime.**
Desta vez é o fim de uma fatia de dados.
Para obter mais informações sobre **objetos DateTime,** `Get-Help Get-Date` digite.
*EndDateTime* deve ser especificado no formato ISO8601, como nos exemplos a seguir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Hora Padrão do Pacífico) O designador de fuso horário padrão é UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Esse cmdlet modifica o status das fatias que pertencem ao grupo especificado por esse parâmetro.

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

### -StartDateTime
Especifica o início de um período de tempo como um **objeto DateTime.**
Este é o início de uma fatia de dados.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Especifica um status a ser atribuído à fatia de dados.
Os valores aceitáveis para este parâmetro são:
- Esperando.
A fatia de dados está aguardando validação em relação às políticas de validação antes de ser processada. 
- Pronto.
O processamento de dados foi concluído e a fatia de dados está pronta.
- Inprogress.
O processamento de dados está em andamento. 
- Falhou.
Falha no processamento de dados.
- Ignorada.
Ignorada a processamento da fatia de dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Especifica o tipo de atualização da fatia.
Os valores aceitáveis para este parâmetro são:
- Individuais.
Define o status de cada fatia para o conjunto de dados no intervalo de tempo especificado. 
- UpstreamInStreamLine.
Define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes, que são usados como conjuntos de dados de entrada para atividades no pipeline.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## Saídas

### System.Boolean

## Notas
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data,

## LINKS RELACIONADOS

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


