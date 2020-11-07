---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
ms.openlocfilehash: 95865de8e99ad09a755329b742f69ebe1e935d72
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785183"
---
# <span data-ttu-id="6fb5f-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="6fb5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb5f-103">Cria uma regra de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fb5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fb5f-104">SYNTAX</span></span>

### <span data-ttu-id="6fb5f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb5f-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb5f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6fb5f-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb5f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fb5f-107">DESCRIPTION</span></span>
<span data-ttu-id="6fb5f-108">O cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="6fb5f-109">Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="6fb5f-110">As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="6fb5f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fb5f-111">EXAMPLES</span></span>

### <span data-ttu-id="6fb5f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fb5f-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="6fb5f-113">Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="6fb5f-114">Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="6fb5f-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="6fb5f-116">Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="6fb5f-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="6fb5f-118">O quinto comando usa **Add-AzureRmApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="6fb5f-119">OS</span><span class="sxs-lookup"><span data-stu-id="6fb5f-119">PARAMETERS</span></span>

### <span data-ttu-id="6fb5f-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6fb5f-120">-BackendAddressPool</span></span>
<span data-ttu-id="6fb5f-121">Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="6fb5f-122">Você pode criar essa referência de objeto usando o cmdlet New-AzureRmApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="6fb5f-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="6fb5f-123">O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="6fb5f-124">Observe que o endereço IP fica entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="6fb5f-125">A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="6fb5f-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="6fb5f-126">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="6fb5f-127">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="6fb5f-128">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="6fb5f-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6fb5f-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="6fb5f-130">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="6fb5f-131">As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzureRmApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="6fb5f-132">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="6fb5f-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="6fb5f-133">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6fb5f-133">For instance:</span></span>

<span data-ttu-id="6fb5f-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="6fb5f-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="6fb5f-135">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="6fb5f-136">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="6fb5f-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6fb5f-137">-BackendHttpSettings</span></span>
<span data-ttu-id="6fb5f-138">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="6fb5f-139">Você pode criar essa referência de objeto usando o cmdlet New-AzureRmApplicationGatewayBackendHttpSettings e a sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="6fb5f-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="6fb5f-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="6fb5f-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="6fb5f-141">A variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="6fb5f-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="6fb5f-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="6fb5f-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="6fb5f-143">As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="6fb5f-144">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="6fb5f-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6fb5f-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6fb5f-146">Especifica a ID de uma coleção de configurações HTTP de back-end existente que pode ser adicionada às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="6fb5f-147">As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="6fb5f-148">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="6fb5f-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="6fb5f-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6fb5f-149">For instance:</span></span>

<span data-ttu-id="6fb5f-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="6fb5f-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="6fb5f-151">As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="6fb5f-152">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="6fb5f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb5f-153">-DefaultProfile</span></span>
<span data-ttu-id="6fb5f-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb5f-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fb5f-155">-Name</span></span>
<span data-ttu-id="6fb5f-156">Especifica o nome da configuração de regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6fb5f-157">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="6fb5f-157">-Paths</span></span>
<span data-ttu-id="6fb5f-158">Especifica uma ou mais regras de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="6fb5f-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fb5f-159">-RedirectConfiguration</span></span>
<span data-ttu-id="6fb5f-160">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6fb5f-160">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6fb5f-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6fb5f-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="6fb5f-162">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fb5f-162">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6fb5f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb5f-163">CommonParameters</span></span>
<span data-ttu-id="6fb5f-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb5f-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb5f-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb5f-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fb5f-166">INPUTS</span></span>

###  
<span data-ttu-id="6fb5f-167">**New-AzureRmApplicationGatewayPathRuleConfig** não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="6fb5f-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="6fb5f-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fb5f-168">OUTPUTS</span></span>

###  
<span data-ttu-id="6fb5f-169">**New-AzureRmApplicationGatewayPathRuleConfig** cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="6fb5f-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="6fb5f-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fb5f-170">NOTES</span></span>

## <span data-ttu-id="6fb5f-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fb5f-171">RELATED LINKS</span></span>

[<span data-ttu-id="6fb5f-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6fb5f-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6fb5f-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="6fb5f-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6fb5f-175">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6fb5f-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6fb5f-176">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6fb5f-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="6fb5f-177">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="6fb5f-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6fb5f-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="6fb5f-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6fb5f-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


