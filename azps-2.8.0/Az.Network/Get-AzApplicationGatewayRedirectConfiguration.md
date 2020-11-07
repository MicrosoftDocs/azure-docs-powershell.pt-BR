---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 79a4e76f4c9ece74c25c8f017fab6840aac63a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771796"
---
# Get-AzApplicationGatewayRedirectConfiguration

## Sinopse
Obtém uma configuração de redirecionamento existente de um aplicativo gateway.

## SYNTAX

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzApplicationGatewayRedirectConfiguration** Obtém uma configuração de redirecionamento existente de um aplicativo gateway.

## EXEMPLOS

### Exemplo 1
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.
O segundo comando obtém a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado na variável chamada $AppGW.

## OS

### -ApplicationGateway
O applicationGateway

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

### -Nome
O nome da regra de roteamento de solicitação

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration

## INFORMA

## LINKS RELACIONADOS

[Add-AzApplicationGatewayRedirectConfiguration](./Add-AzApplicationGatewayRedirectConfiguration.md)

[New-AzApplicationGatewayRedirectConfiguration](./New-AzApplicationGatewayRedirectConfiguration.md)

[Remove-AzApplicationGatewayRedirectConfiguration](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[Set-AzApplicationGatewayRedirectConfiguration](./Set-AzApplicationGatewayRedirectConfiguration.md)
