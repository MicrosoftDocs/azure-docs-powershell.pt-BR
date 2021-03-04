---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893139"
---
# New-AzApplicationGatewayRewriteRule

## SYNOPSIS
Cria uma regra de reescrita para um gateway de aplicativo.

## SINTAXE

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzApplicationGatewayRewriteRule** cria uma regra de regra de regra para um gateway de aplicativo do Azure.

## EXEMPLOS

### Exemplo 1 : Criar uma regra de regra para um gateway de aplicativo
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

Este comando cria uma regra de regra1 e armazena o resultado na variável chamada $rule.

## PARÂMETROS

### -ActionSet
ActionSet da regra de reescrita

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition
Condição para a regra de reescrita ser executada

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
O nome do ReescritaRule

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

### -RuleSequence
A ordem de regra dessa regra de regra de reescrita no conjunto de regras de regra de reescrita

```yaml
Type: System.Int32
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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule

## NOTES

## LINKS RELACIONADOS

[Add-AzApplicationGatewayRewriteRuleSet](./Add-AzApplicationGatewayRewriteRuleSet.md)

[Get-AzApplicationGatewayRewriteRuleSet](./Get-AzApplicationGatewayRewriteRuleSet.md)

[New-AzApplicationGatewayRewriteRuleSet](./New-AzApplicationGatewayRewriteRuleSet.md)

[Remove-AzApplicationGatewayRewriteRuleSet](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[Set-AzApplicationGatewayRewriteRuleSet](./Set-AzApplicationGatewayRewriteRuleSet.md)

[New-AzApplicationGatewayRewriteRuleActionSet](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[New-AzApplicationGatewayRewriteRuleHeaderConfiguration](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
