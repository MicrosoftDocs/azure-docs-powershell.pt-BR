---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775427"
---
# <span data-ttu-id="58232-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58232-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="58232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58232-102">SYNOPSIS</span></span>
<span data-ttu-id="58232-103">Cria uma regra de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58232-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="58232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58232-104">SYNTAX</span></span>

### <span data-ttu-id="58232-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58232-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58232-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="58232-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58232-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58232-107">DESCRIPTION</span></span>
<span data-ttu-id="58232-108">O cmdlet **New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58232-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="58232-109">Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="58232-110">As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="58232-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58232-111">EXAMPLES</span></span>

### <span data-ttu-id="58232-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58232-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="58232-113">Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58232-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="58232-114">Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="58232-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="58232-116">Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="58232-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="58232-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="58232-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="58232-118">O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="58232-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="58232-119">OS</span><span class="sxs-lookup"><span data-stu-id="58232-119">PARAMETERS</span></span>

### <span data-ttu-id="58232-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58232-120">-BackendAddressPool</span></span>
<span data-ttu-id="58232-121">Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="58232-122">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="58232-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="58232-123">O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="58232-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="58232-124">Observe que o endereço IP fica entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="58232-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="58232-125">A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="58232-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="58232-126">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="58232-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="58232-127">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="58232-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="58232-128">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="58232-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="58232-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="58232-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="58232-130">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="58232-131">As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="58232-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="58232-132">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="58232-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="58232-133">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="58232-133">For instance:</span></span>

<span data-ttu-id="58232-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="58232-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="58232-135">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="58232-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="58232-136">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="58232-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="58232-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="58232-137">-BackendHttpSettings</span></span>
<span data-ttu-id="58232-138">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="58232-139">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSetting e a sintaxe semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="58232-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="58232-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "ContosoHttpSetings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="58232-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="58232-141">A variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="58232-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="58232-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="58232-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="58232-143">As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="58232-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="58232-144">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="58232-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="58232-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="58232-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="58232-146">Especifica a ID de uma coleção de configurações HTTP de back-end existente que pode ser adicionada às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="58232-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="58232-147">As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendHttpSetting.</span><span class="sxs-lookup"><span data-stu-id="58232-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="58232-148">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="58232-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="58232-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="58232-149">For instance:</span></span>

<span data-ttu-id="58232-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="58232-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="58232-151">As configurações HTTP de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="58232-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="58232-152">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="58232-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="58232-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58232-153">-DefaultProfile</span></span>
<span data-ttu-id="58232-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58232-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58232-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="58232-155">-Name</span></span>
<span data-ttu-id="58232-156">Especifica o nome da configuração de regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="58232-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="58232-157">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="58232-157">-Paths</span></span>
<span data-ttu-id="58232-158">Especifica uma ou mais regras de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58232-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="58232-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="58232-159">-RedirectConfiguration</span></span>
<span data-ttu-id="58232-160">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="58232-160">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="58232-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="58232-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="58232-162">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="58232-162">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="58232-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58232-163">CommonParameters</span></span>
<span data-ttu-id="58232-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58232-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58232-165">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58232-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58232-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58232-166">INPUTS</span></span>

###  
<span data-ttu-id="58232-167">**New-AzApplicationGatewayPathRuleConfig** não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="58232-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="58232-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58232-168">OUTPUTS</span></span>

###  
<span data-ttu-id="58232-169">**New-AzApplicationGatewayPathRuleConfig** cria novas instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="58232-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="58232-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58232-170">NOTES</span></span>

## <span data-ttu-id="58232-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58232-171">RELATED LINKS</span></span>

[<span data-ttu-id="58232-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="58232-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="58232-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58232-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="58232-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="58232-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="58232-175">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58232-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="58232-176">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="58232-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="58232-177">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="58232-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="58232-178">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="58232-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="58232-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="58232-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="58232-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="58232-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


