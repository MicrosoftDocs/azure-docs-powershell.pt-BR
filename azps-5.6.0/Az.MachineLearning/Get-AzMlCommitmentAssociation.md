---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 9d58d8385d3f1d02e3bd823f43403d7dcdacf4a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893270"
---
# Get-AzMlCommitmentAssociation

## SYNOPSIS
Recupera as informações de resumo para uma ou mais associações de compromisso.

## SINTAXE

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
Recupera informações de associação de compromisso.
Dependendo dos parâmetros passados, o cmdlet retorna uma associação de compromisso específica ou uma coleção de associações de compromisso para o plano de compromisso especificado.

## EXEMPLOS

### Exemplo 1: obter uma associação de compromisso específica
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### Exemplo 2: Obter todas as associações de compromisso para o plano de compromisso especificado
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## PARÂMETROS

### -CommitmentPlanName
O nome do plano de compromisso do Azure ML que tem uma ou mais associações de compromisso.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
O nome da associação de compromisso do Azure ML.

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
O nome do grupo de recursos para a associação de compromisso do Azure ML.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan

## NOTES
Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKS RELACIONADOS
