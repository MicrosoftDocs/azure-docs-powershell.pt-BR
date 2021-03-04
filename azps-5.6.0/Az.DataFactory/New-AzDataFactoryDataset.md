---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: b78d1ef78d7da1f8ad035951174578766de6a4a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888261"
---
# New-AzDataFactoryDataset

## SYNOPSIS
Cria um conjuntos de dados no Data Factory.

## SINTAXE

### ByFactoryName (Padrão)
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzDataFactoryDataset** cria um conjuntos de dados no Azure Data Factory.
Se você especificar um nome para um conjuntos de dados que já existe, este cmdlet solicitará a confirmação antes de substituir o conjuntos de dados.
Se você especificar o *parâmetro Force,* o cmdlet substituirá o conjuntos de dados existente sem confirmação.
Execute essas operações na seguinte ordem: 
- Criar uma fábrica de dados. 
- Criar serviços vinculados. 
- Criar conjuntos de dados. 
- Criar um pipeline.
Se um conjuntos de dados com o mesmo nome já existir no fábrica de dados, esse cmdlet solicitará que você confirme se deve substituir o conjuntos de dados existente com o novo conjuntos de dados.
Se você confirmar a substituição do conjuntos de dados existente, a definição do conjuntos de dados também será substituída.

## EXEMPLOS

### Exemplo 1: Criar um conjuntos de dados
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

Este comando cria um grupo de dados chamado DA_WikipediaClickEvents no fábrica de dados chamado WikiADF.
O comando baseia o conjuntos de dados em informações no arquivo DAWikipediaClickEvents.json.

### Exemplo 2: Exibir disponibilidade para um novo conjuntos de dados
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

O primeiro comando cria um grupo de dados chamado DA_WikipediaClickEvents, como em um exemplo anterior, e atribui esse conjuntos de dados à variável $Dataset.
O segundo comando usa a notação de ponto padrão para exibir detalhes sobre a propriedade Availability do conjuntos de dados.

### Exemplo 3: Exibir local para um novo conjuntos de dados
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

O primeiro comando cria um grupo de dados chamado DA_WikipediaClickEvents, como em um exemplo anterior, e atribui esse conjuntos de dados à variável $Dataset.
O segundo comando exibe detalhes sobre a propriedade Location do conjuntos de dados.

### Exemplo 4: Exibir regras de validação para um novo conjunto de dados
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

O primeiro comando cria um grupo de dados chamado DA_WikipediaClickEvents, como em um exemplo anterior, e atribui esse conjuntos de dados à variável $Dataset.
O segundo comando obtém detalhes sobre as regras de validação para o conjunto de dados e as passa para o cmdlet Format-List usando o operador de pipeline.
Esse Windows PowerShell cmdlet formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

## PARÂMETROS

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet cria um conjuntos de dados no fábrica de dados especificado por esse parâmetro.

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
Este cmdlet cria um conjuntos de dados no fábrica de dados especificado por esse parâmetro.

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

### -File
Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do conjuntos de dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet substitui um conjuntos de dados existente sem solicitar a confirmação.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Especifica o nome do conjuntos de dados a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Este cmdlet cria um conjunto de dados no grupo especificado por esse parâmetro.

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataset

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[Get-AzDataFactoryDataset](./Get-AzDataFactoryDataset.md)

[Remove-AzDataFactoryDataset](./Remove-AzDataFactoryDataset.md)


