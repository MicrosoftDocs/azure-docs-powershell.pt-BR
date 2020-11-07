---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785336"
---
# Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration

## Sinopse
Obtém a configuração WAF de um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** Obtém a configuração WAF (firewall de aplicativo Web) de um gateway de aplicativo.

## EXEMPLOS

### Exemplo 1: obter uma configuração de firewall de aplicativo Web do aplicativo Web Gateway
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e, em seguida, armazena-o na variável $AppGW.

O segundo comando obtém a configuração de firewall do gateway do aplicativo em $AppGW e, em seguida, armazena-a no $FirewallConfig.

## OS

### -ApplicationGateway
Especifica um objeto do gateway do aplicativo.
Você pode usar o cmdlet Get-AzureRmApplicationGateway para obter um objeto de gateway de aplicativo.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
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

### PSApplicationGateway
O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


