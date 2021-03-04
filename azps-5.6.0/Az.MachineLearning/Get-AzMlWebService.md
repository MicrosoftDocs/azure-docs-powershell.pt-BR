---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 1dcf881fbe0a3a616a7522236099f7698b50a1a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892624"
---
# Get-AzMlWebService

## SYNOPSIS
Recupera as informações de resumo de um ou mais serviços Web.

## SINTAXE

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
Recupera informações de definição de serviço Web.
Dependendo dos parâmetros passados, o cmdlet retorna a definição de um serviço Web específico, uma coleção de definições para os serviços Web para um grupo de recursos especificado dentro da assinatura atual ou uma coleção de definições para os serviços Web dentro da assinatura atual.

## EXEMPLOS

### Exemplo 1: Obter detalhes do serviço Web específico
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### Exemplo 2: Obter todos os recursos do serviço Web na assinatura atual
```
Get-AzMlWebService
```

### Exemplo 3: Obter todos os serviços Web na assinatura atual e determinado grupo de recursos
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## PARÂMETROS

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
O nome do serviço Web para o qual os detalhes são recuperados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
O nome da região

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos do qual os detalhes do serviço Web são recuperados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTES
Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKS RELACIONADOS
