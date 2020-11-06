---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: 27e5715f32b631fff3f185f0925d0b2a85967ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427876"
---
# Get-AzureRmApplicationGatewayAvailableWafRuleSets

## Sinopse
Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** Obtém todos os conjuntos de regras de firewall do aplicativo Web disponíveis.

## EXEMPLOS

### Exemplo 1
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

Esses comandos retornam todos os conjuntos de regras de firewall do aplicativo Web disponíveis.

## OS

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

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult

## INFORMA
**List-AzureRmApplicationGatewayAvailableWafRuleSets** é um alias para o cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .

## LINKS RELACIONADOS

