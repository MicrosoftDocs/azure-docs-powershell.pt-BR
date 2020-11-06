---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 9fd01fdf63a0c58599c00a6a6739802efb5304d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600416"
---
# New-AzApplicationGatewayFirewallDisabledRuleGroupConfig

## Sinopse
Cria uma nova configuração de grupo de regras desabilitada.

## SYNTAX

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cria uma nova configuração de grupo de regras desabilitada.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

O comando cria uma nova configuração de grupo de regras desabilitada para o grupo de regras chamado "REQUEST-942-APPLICATION-ATTACK-SQLI" com a regra 942130 e a regra 942140 sendo desabilitada. A nova configuração do grupo de regras desabilitadas é salva no $disabledRuleGroup 1.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -RuleGroupName
O nome do grupo de regras que será desabilitado.

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

### -Regras
A lista de regras que será desabilitada.
Se for nulo, todas as regras do grupo de regras serão desabilitadas.

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup

## INFORMA

## LINKS RELACIONADOS

[New-AzApplicationGatewayWebApplicationFirewallConfiguration](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

