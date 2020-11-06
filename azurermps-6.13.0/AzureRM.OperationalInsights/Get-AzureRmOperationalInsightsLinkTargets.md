---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428433"
---
# Get-AzureRmOperationalInsightsLinkTargets

## Sinopse
Obtém contas que não estão associadas a uma assinatura.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmOperationalInsightsLinkTargets** lista contas existentes que não estão associadas a uma assinatura do Azure.
Para vincular um novo espaço de trabalho a uma conta existente, use uma ID de cliente retornada por essa operação na propriedade ID do cliente de um novo espaço de trabalho.

## EXEMPLOS

### Exemplo 1: obter contas não vinculadas
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

Esse comando obtém contas não vinculadas que pertencem à identificação do chamador.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount

## INFORMA

## LINKS RELACIONADOS

[Cmdlets do Azure Operational insights](./AzureRM.OperationalInsights.md)


