---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115865"
---
# Get-AzDataFactoryLinkedService

## Sinopse
Obtém informações sobre serviços vinculados no Azure Data Factory.

## Sintaxe

### ByFactoryName (Default)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzDataFactoryLinkedService** obtém informações sobre serviços vinculados no Azure Data Factory.
Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.
Se você não especificar um nome, este cmdlet obterá informações sobre todos os serviços vinculados na fábrica de dados.

## Exemplos

### Exemplo 1: Obter informações sobre todos os serviços vinculados
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Esse comando obtém informações sobre todos os serviços vinculados no fábrica de dados chamado WikiADF e passa os serviços vinculados para o cmdlet Format-List usando o operador de pipeline.
Esse cmdlet formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

### Exemplo 2: Obter informações sobre um serviço vinculado específico
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Este comando obtém informações sobre o serviço vinculado chamado HDILinkedService na fábrica de dados chamada WikiADF.

### Exemplo 3: obter informações sobre um serviço vinculado específico especificando o parâmetro DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

O primeiro comando usa o cmdlet Get-AzDataFactory para obter o fábrica de dados chamado ContosoFactory e, em seguida, armazena-o na variável $DataFactory.
O segundo comando obtém informações sobre o serviço vinculado do fábrica de dados armazenado no $DataFactory e passa essas informações para o cmdlet Format-Table usando o operador de pipeline.
**Formatar Tabela** formatará a saída como um conjuntos de dados com as propriedades especificadas como colunas de conjuntos de dados.

## Parâmetros

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet obtém serviços vinculados que pertencem ao fábrica de dados especificado por esse parâmetro.

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
Este cmdlet obtém serviços vinculados que pertencem ao fábrica de dados especificado por esse parâmetro.

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

### -Nome
Especifica o nome do serviço vinculado sobre o qual obter informações.

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
Este cmdlet obtém serviços vinculados que pertencem ao grupo especificado por esse parâmetro.

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

## Entradas

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## Saídas

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## Notas
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data,

## LINKS RELACIONADOS

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


