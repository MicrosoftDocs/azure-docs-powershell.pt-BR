---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890798"
---
# Get-AzApplicationGatewayWebApplicationFirewallConfiguration

## SYNOPSIS
Obtém a configuração WAF de um gateway de aplicativo.

## SINTAXE

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** obtém a configuração do waf (firewall de aplicativo web) de um gateway de aplicativo.

## EXEMPLOS

### Exemplo 1: obter uma configuração de firewall de aplicativo web de gateway de aplicativo
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGW aplicativo.
O segundo comando obtém a configuração de firewall do gateway de aplicativo no $AppGW e o armazena $FirewallConfig.

## PARÂMETROS

### -ApplicationGateway
Especifica um objeto gateway de aplicativo.
Você pode usar o cmdlet Get-AzApplicationGateway para obter um objeto gateway de aplicativo.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration

## NOTES

## LINKS RELACIONADOS

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[New-AzApplicationGatewayWebApplicationFirewallConfiguration](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


