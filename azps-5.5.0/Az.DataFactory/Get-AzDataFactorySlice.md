---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118823"
---
# Get-AzDataFactorySlice

## Sinopse
Obtém fatias de dados para um conjuntos de dados no Azure Data Factory.

## Sintaxe

### ByFactoryName (Default)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzDataFactorySlice** obtém fatias de dados para um conjuntos de dados no Azure Data Factory.
Especifique uma hora de início e uma hora de término para definir um intervalo de fatias de dados a exibir.
O status de uma fatia de dados é um dos seguintes valores: 
- PendenteExecução.
O processamento de dados não foi iniciado. 
- Inprogress.
O processamento de dados está em andamento. 
- Pronto.
O processamento de dados está concluído.
A fatia de dados está pronta para que as fatias dependentes a consumam. 
- Falhou.
A correção que produz a fatia falhou. 
- Ignorar.
A Data Factory ignora o processamento da fatia. 
- Repetir.
A Data Factory recupera a executar que produz a fatia. 
- Tempo de tempo. O processamento de dados deu um tempo. 
- PendenteValidation.
A fatia de dados está aguardando validação antes de ser processada. 
- Tentar validação novamente.
A Data Factory recupera a validação da fatia. 
- Falha na Validação.
Falha na validação da fatia.
Para cada uma das fatias, você pode ver mais informações sobre a operação que produz a fatia usando o cmdlet Get-AzDataFactoryRun dados.

## Exemplos

### Exemplo 1: Obter fatias de dados para um conjuntos de dados
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

Esse comando obtém todas as fatias de dados do grupo de dados chamado WikiAggregatedData na fábrica de dados chamada WikiADF.
O comando obtém fatias produzidas após o tempo especificado pelo parâmetro StartDateTime.
O código de exemplo a seguir define a disponibilidade para esse conjunto de dados a cada hora no arquivo JavaScript Object Notation (JSON).
disponibilidade: { ponto: "Hora", pontoMultiplier: 1 } Alguns dos resultados estão Prontos e outros sãoPendingExecution.
As fatias prontas já foram executados.
As fatias pendentes estão aguardando para ser executados no final de cada hora no intervalo especificado pelo cmdlet Set-AzDataFactoryPipelineActivePeriod dados.
Neste exemplo, os períodos de início e de término do pipeline e a fatia têm um valor de um dia (24 horas).

### Exemplo 2

Obtém fatias de dados para um conjuntos de dados no Azure Data Factory. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## Parâmetros

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet obtém fatias que pertencem à fábrica de dados especificada por esse parâmetro.

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
Este cmdlet obtém fatias que pertencem à fábrica de dados especificada por esse parâmetro.

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
Especifica o nome do conjuntos de dados para o qual este cmdlet obtém fatias.

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
Esse cmdlet obtém as fatias produzidas antes do tempo especificado por esse parâmetro.
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
Este cmdlet obtém fatias que pertencem ao grupo especificado por esse parâmetro.

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
Esse cmdlet obtém fatias produzidas após o tempo especificado por esse parâmetro.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## Saídas

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## Notas
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data,

## LINKS RELACIONADOS

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


