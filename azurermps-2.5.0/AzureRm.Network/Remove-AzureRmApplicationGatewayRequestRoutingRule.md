---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785479"
---
# Remove-AzureRmApplicationGatewayRequestRoutingRule

## Sinopse
Remove uma regra de roteamento de solicitação de um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** remove uma regra de roteamento de solicitação de um gateway do aplicativo do Azure.

## EXEMPLOS

### Exemplo 1: remover uma regra de roteamento de solicitação de um aplicativo gateway
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.

O segundo comando Remove a regra de roteamento de solicitação chamada Rule02 do gateway do aplicativo armazenado em $AppGw.

## OS

### -ApplicationGateway
Especifica o gateway do aplicativo do qual remover uma regra de roteamento de solicitações.

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

### -Nome
Especifica o nome da regra de roteamento de solicitação para a qual esse cmdlet Remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApplicationGatewayRequestRoutingRule](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[Get-AzureRmApplicationGatewayRequestRoutingRule](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[New-AzureRmApplicationGatewayRequestRoutingRule](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[Set-AzureRmApplicationGatewayRequestRoutingRule](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


