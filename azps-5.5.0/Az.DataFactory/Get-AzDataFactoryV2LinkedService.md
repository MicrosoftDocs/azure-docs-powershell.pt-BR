---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113878"
---
# Get-AzDataFactoryV2LinkedService

## Sinopse
Obtém informações sobre serviços vinculados no Data Factory.

## Sintaxe

### ByFactoryName (Default)
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O Get-AzDataFactoryV2LinkedService cmdlet obtém informações sobre serviços vinculados no Azure Data Factory.
Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.
Se você não especificar um nome, este cmdlet obterá informações sobre todos os serviços vinculados na fábrica de dados.

## Exemplos

### Exemplo 1: Obter informações sobre todos os serviços vinculados
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Esse comando obtém informações sobre todos os serviços vinculados no fábrica de dados chamado WikiADF e passa os serviços vinculados para o cmdlet Format-List usando o operador de pipeline.
Esse cmdlet do Windows PowerShell formata os resultados.
Para obter mais informações, digite Get-Help Formatar Lista.
Você pode usar uma das seguintes maneiras:

### Exemplo 2: Obter informações sobre um serviço vinculado específico
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

Este comando obtém informações sobre o serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamada WikiADF.

### Exemplo 3: obter informações sobre um serviço vinculado específico especificando o parâmetro DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

O primeiro comando usa o cmdlet Get-AzDataFactoryV2 para obter o fábrica de dados chamado ContosoFactory e, em seguida, armazena-o na variável $DataFactory.
O segundo comando obtém informações sobre o serviço vinculado do fábrica de dados armazenado no $DataFactory e passa essas informações para o cmdlet Format-Table usando o operador de pipeline.
O Format-Table cmdlet formata a saída como um conjuntos de dados com as propriedades especificadas como colunas de conjuntos de dados.

## Parâmetros

### -DataFactory
Especifica um objeto PSDataFactory.
Este cmdlet obtém serviços vinculados que pertencem ao fábrica de dados especificado por esse parâmetro.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

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

### -ResourceId
A ID de recurso do Azure.

```yaml
Type: System.String
Parameter Sets: ByResourceId
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

### System.String

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory

## Saídas

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService

## Notas
Palavras-chave: azure, azurerm, arm, resource, management, manager, data,

## LINKS RELACIONADOS

[Set-AzDataFactoryV2LinkedService]()

[Remove-AzDataFactoryV2LinkedService]()
