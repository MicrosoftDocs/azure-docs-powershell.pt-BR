---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 209986a25882415a68df86611d10559612a8ec04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432453"
---
# New-AzureRmApplicationGatewayPathRuleConfig

## Sinopse
Cria uma regra de caminho do gateway do aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SetByResourceId
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.
Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.

As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.

## EXEMPLOS

### Exemplo 1
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.
Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.
Essa referência de objeto é armazenada em uma variável chamada $Gateway.

Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.

O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.

O quinto comando usa **Add-AzureRmApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.

## OS

### -BackendAddressPool
Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.
Você pode criar essa referência de objeto usando o cmdlet New-AzureRmApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta:

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.
Observe que o endereço IP fica entre aspas e separado por vírgulas.

A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .

O pool de endereços back-end representa os endereços IP nos servidores back-end.
Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às definições de configuração de regra de caminho de gateway.
As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzureRmApplicationGatewayBackendAddressPool.
Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .
Por exemplo:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

O pool de endereços back-end representa os endereços IP nos servidores back-end.
Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de regra de caminho de gateway.
Você pode criar essa referência de objeto usando o cmdlet New-AzureRmApplicationGatewayBackendHttpSettings e a sintaxe semelhante a esta:

$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled"

A variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :

-DefaultBackendHttpSettings $HttpSettings

As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Especifica a ID de uma coleção de configurações HTTP de back-end existente que pode ser adicionada às definições de configuração de regra de caminho de gateway.
As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings.
Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .
Por exemplo:

-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.

```yaml
Type: String
Parameter Sets: SetByResourceId
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
Especifica o nome da configuração de regra de caminho que este cmdlet cria.

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

### -Caminhos
Especifica uma ou mais regras de caminho do gateway do aplicativo.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration do gateway do aplicativo

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
ID do aplicativo do gateway de RedirectConfiguration

```yaml
Type: String
Parameter Sets: SetByResourceId
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

###  
**New-AzureRmApplicationGatewayPathRuleConfig** não aceita entrada em pipeline.

## EXIBE

###  
**New-AzureRmApplicationGatewayPathRuleConfig** cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayUrlPathMapConfig](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[New-AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[New-AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[New-AzureRmApplicationGatewayPathRuleConfig](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[New-AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Remove-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Set-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


