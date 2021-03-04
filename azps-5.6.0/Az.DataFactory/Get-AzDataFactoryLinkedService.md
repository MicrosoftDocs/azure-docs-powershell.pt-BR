---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888313"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Obtém informações sobre serviços vinculados no Azure Data Factory.

## SINTAXE

### ByFactoryName (Padrão)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzDataFactoryLinkedService** obtém informações sobre serviços vinculados no Azure Data Factory.
Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.
Se você não especificar um nome, este cmdlet obterá informações sobre todos os serviços vinculados no fábrica de dados.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os serviços vinculados
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

Este comando obtém informações sobre todos os serviços vinculados no fábrica de dados chamado WikiADF e, em seguida, passa os serviços vinculados para o cmdlet Format-List usando o operador de pipeline.
Esse cmdlet formata os resultados.
Para obter mais informações, digite `Get-Help Format-List` .

### Exemplo 2: obter informações sobre um serviço vinculado específico
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

Este comando obtém informações sobre o serviço vinculado chamado HDILinkedService no fábrica de dados chamado WikiADF.

### Exemplo 3: obter informações sobre um serviço vinculado específico especificando o parâmetro DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

O primeiro comando usa o cmdlet Get-AzDataFactory para obter o fábrica de dados chamado ContosoFactory e, em seguida, o armazena na variável $DataFactory.
O segundo comando obtém informações sobre o serviço vinculado para o fábrica de dados armazenado no $DataFactory e, em seguida, passa essas informações para o cmdlet Format-Table usando o operador de pipeline.
**Format-Table** formatará a saída como um conjuntos de dados com as propriedades especificadas como colunas de conjuntos de dados.

## PARÂMETROS

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

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


