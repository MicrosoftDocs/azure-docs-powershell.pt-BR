---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432204"
---
# Get-AzureRmMlCommitmentPlan

## Sinopse
Recupera as informações resumidas para um ou mais planos de compromisso.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Recupera informações do plano de compromisso.
Dependendo dos canceladores passados, o cmdlet retorna um plano de compromisso específico, uma coleção de planos de compromisso para um grupo de recursos especificado na assinatura atual ou um conjunto de planos de compromisso dentro da assinatura atual.

## EXEMPLOS

### --------------------------Exemplo 1: obter um plano de compromisso específico--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### --------------------------Exemplo 2: obter todos os recursos de plano de compromisso na assinatura atual--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan
```

### --------------------------Exemplo 3: obter todos os planos de compromisso na assinatura atual e o grupo de recursos fornecido--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## OS

### -Nome
O nome do plano de compromisso.

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
O nome do grupo de recursos para o plano de compromisso do Azure ML.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan
Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []

## INFORMA
Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml

## LINKS RELACIONADOS

