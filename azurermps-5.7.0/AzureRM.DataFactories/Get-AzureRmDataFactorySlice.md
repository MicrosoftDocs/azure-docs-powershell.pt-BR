---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426744"
---
# Get-AzureRmDataFactorySlice

## Sinopse
Obtém fatias de dados para um conjunto de dados no Azure data Factory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByFactoryName (padrão)
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDataFactorySlice** Obtém fatias de dados de um conjunto de dados no Azure data Factory.
Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a serem exibidas.

O status de uma fatia de dados é um dos seguintes valores: 

- PendingExecution.
O processamento de dados não foi iniciado. 
- InProgress.
O processamento de dados está em andamento. 
- Está.
O processamento de dados foi concluído.
A fatia de dados está pronta para fatias dependentes para consumi-la. 
- Conseguiu.
Falha na execução que produz a fatia. 
- Siga.
O data Factory ignora o processamento da fatia. 
- Executar.
O realocador de dados repete a execução que produz a fatia. 
- Tempo limite esgotado. O processamento de dados expirou. 
- PendingValidation.
A fatia de dados está aguardando a validação antes de ser processada. 
- Tente validar novamente.
O realocador de dados repete a validação da fatia. 
- Falha na validação.
Falha na validação da fatia.

Para cada uma das fatias, você pode ver mais informações sobre a execução que produz a fatia usando o cmdlet Get-AzureRmDataFactoryRun.

## EXEMPLOS

### Exemplo 1: obter fatias de dados de um conjunto de dados
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Esse comando obtém todas as fatias de dados para o conjunto de dados chamado WikiAggregatedData no data Factory chamado WikiADF.
O comando obtém as fatias produzidas após a hora em que o parâmetro StartDatetime especifica.
O código de exemplo a seguir define a disponibilidade desse conjunto de código a cada hora no arquivo JSON (JavaScript Object Notation).

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
As fatias prontas já foram executadas.
As faixas pendentes estão aguardando para serem executadas no final de cada hora no intervalo especificado pelo cmdlet de Set-AzureRmDataFactoryPipelineActivePeriod.
Neste exemplo, os períodos de início e término do pipeline e a fatia têm um valor de um dia (24 horas).

## OS

### -Datafactory
Especifica um objeto **PSDataFactory** .
Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.

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
Esse cmdlet obtém as fatias que pertencem à fábrica de dados que esse parâmetro especifica.

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
Especifica o nome do DataSet para o qual esse cmdlet obtém fatias.

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
Esse cmdlet obtém as fatias geradas antes do tempo que esse parâmetro especifica.
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
Esse cmdlet obtém as fatias que pertencem ao grupo especificado por esse parâmetro.

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
Esse cmdlet obtém as fatias produzidas após o momento em que esse parâmetro especifica.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## INFORMA
* Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[Set-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Set-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


