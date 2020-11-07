---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: cbd69ff20e32d93ff5d9f9f7c4959568f627c7e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944804"
---
# New-AzApplicationGatewayPathRuleConfig

## Sinopse
Cria uma regra de caminho do gateway do aplicativo.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.
Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.
As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.

## EXEMPLOS

### Exemplo 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.
Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.
Essa referência de objeto é armazenada em uma variável chamada $Gateway.
Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.
O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.
O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.

### Exemplo 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

Esse comando cria uma regra de caminho com o nome "base", trajetórias como "/base", BackendAddressPool como $AddressPool, BackendHttpSettings como $HttpSettings e FirewallPolicy como $firewallPolicy. NGS e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.

## OS

### -BackendAddressPool
Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.
Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.
Observe que o endereço IP fica entre aspas e separado por vírgulas.
A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .
O pool de endereços back-end representa os endereços IP nos servidores back-end.
Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
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
As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool.
Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .
Por exemplo:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" o pool de endereços de back-end representa os endereços IP nos servidores back-end.
Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.

```yaml
Type: System.String
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
Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSettings e a sintaxe semelhante a esta: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled" a variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings as configurações http de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
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
As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendHttpSettings.
Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .
Por exemplo:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" as configurações HTTP de back-end configurar propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.
Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
Especifica a referência de objeto a uma política de firewall de nível superior. A referência do objeto pode ser criada usando-se New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-The Resource "rgName" uma política de firewall criada usando o commandlet acima pode ser referida em um nível de regra de caminho. o comando acima criaria as configurações de política padrão e as regras gerenciadas.
Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules, respectivamente.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Especifica a ID de um recurso existente de firewall de aplicativo Web de nível superior.
IDs de política de firewall podem ser retornadas usando o cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy. Depois que tivermos a ID, você poderá usar o parâmetro *FirewallPolicyId* em vez do parâmetro *firewallpolicy* .
Por exemplo:-FirewallPolicyId "/subscriptions/<assinatura-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
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
Especifica o nome da configuração de regra de caminho que este cmdlet cria.

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

### -Caminhos
Especifica uma ou mais regras de caminho do gateway do aplicativo.

```yaml
Type: System.String[]
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
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
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
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSet
RewriteRuleSet do gateway do aplicativo

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
ID do aplicativo do gateway de RewriteRuleSet

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule

## INFORMA

## LINKS RELACIONADOS

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSettings](./New-AzApplicationGatewayBackendHttpSettings.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


