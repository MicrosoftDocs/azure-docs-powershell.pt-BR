---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427577"
---
# Set-AzureRmDataFactorySliceStatus

## Sinopse
Define o status das fatias de um conjunto de dados na fábrica de dados do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByFactoryName (padrão)
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDataFactorySliceStatus** define o status das fatias de um conjunto de dados no Azure data Factory.

## EXEMPLOS

### Exemplo 1: definir o status de todas as fatias
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Esse comando define o status de todas as fatias do conjunto de dados chamado DAWikiAggregatedData para aguardar no data Factory chamado WikiADF.
O parâmetro *UpdateType* tem um valor de UpstreamInPipeline e, portanto, o comando define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes.
Conjuntos de dados dependentes são usados como conjuntos de dados de entrada para atividades no pipeline.
Esse comando retorna um valor de $True.

## OS

### -Datafactory
Especifica um objeto **PSDataFactory** .
Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.

```yaml
Type: PSDataFactory
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
Esse cmdlet modifica o status de fatias que pertencem à fábrica de dados que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataSetName
Especifica o nome do DataSet para o qual esse cmdlet modifica fatias.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDateTime
Especifica o fim de um período de tempo como um objeto **DateTime** .
Esta hora é o final de uma fatia de dados.
Para obter mais informações sobre objetos **DateTime** , digite `Get-Help Get-Date` .

*EndDateTime* deve ser especificado no formato ISO8601 como nos exemplos a seguir: 

2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (hora padrão do Pacífico)

O designador de fuso horário padrão é UTC.

```yaml
Type: DateTime
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
Esse cmdlet modifica o status de fatias que pertencem ao grupo especificado por esse parâmetro.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDatetime
Especifica o início de um período de tempo como um objeto **DateTime** .
Esta hora é o início de uma fatia de dados.

```yaml
Type: DateTime
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
Os valores aceitáveis para esse parâmetro são:

- Faxes.
A fatia de dados está aguardando a validação em políticas de validação antes de ser processada. 
- Está.
O processamento de dados foi concluído e a fatia de dados está pronta.
- InProgress.
O processamento de dados está em andamento. 
- Conseguiu.
Falha no processamento de dados.
- Ignorada.
O processamento da fatia de dados foi ignorado.

```yaml
Type: String
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
Especifica o tipo de atualização para a fatia.
Os valores aceitáveis para esse parâmetro são:

- Cada.
Define o status de cada fatia para o conjunto de valores no intervalo de tempo especificado. 
- UpstreamInPipeline.
Define o status de cada fatia para o conjunto de dados e todos os conjuntos de dados dependentes, que são usados como conjuntos de dados de entrada para atividades no pipeline.

```yaml
Type: String
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### System. Boolean

## INFORMA
* Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[Get-AzureRmDataFactorySlice](./Get-AzureRmDataFactorySlice.md)


