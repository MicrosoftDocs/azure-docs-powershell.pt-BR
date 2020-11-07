---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 82940003bbd40cfb15d1f109fbdd1b820d6bd647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771931"
---
# <span data-ttu-id="00bd5-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="00bd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="00bd5-103">Cria uma regra de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00bd5-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="00bd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00bd5-104">SYNTAX</span></span>

### <span data-ttu-id="00bd5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00bd5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bd5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="00bd5-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00bd5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00bd5-107">DESCRIPTION</span></span>
<span data-ttu-id="00bd5-108">O cmdlet **New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00bd5-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="00bd5-109">Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="00bd5-110">As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="00bd5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00bd5-111">EXAMPLES</span></span>

### <span data-ttu-id="00bd5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00bd5-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="00bd5-113">Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00bd5-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="00bd5-114">Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="00bd5-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="00bd5-116">Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="00bd5-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="00bd5-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="00bd5-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="00bd5-118">O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="00bd5-119">OS</span><span class="sxs-lookup"><span data-stu-id="00bd5-119">PARAMETERS</span></span>

### <span data-ttu-id="00bd5-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00bd5-120">-BackendAddressPool</span></span>
<span data-ttu-id="00bd5-121">Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="00bd5-122">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="00bd5-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="00bd5-123">O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="00bd5-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="00bd5-124">Observe que o endereço IP fica entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="00bd5-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="00bd5-125">A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="00bd5-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="00bd5-126">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="00bd5-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="00bd5-127">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="00bd5-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="00bd5-128">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="00bd5-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="00bd5-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="00bd5-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="00bd5-130">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00bd5-131">As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="00bd5-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="00bd5-132">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="00bd5-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="00bd5-133">Por exemplo:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" o pool de endereços de back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="00bd5-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="00bd5-134">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="00bd5-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="00bd5-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00bd5-135">-BackendHttpSettings</span></span>
<span data-ttu-id="00bd5-136">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00bd5-137">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSettings e a sintaxe semelhante a esta: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled" a variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings as configurações http de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="00bd5-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="00bd5-138">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="00bd5-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="00bd5-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="00bd5-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="00bd5-140">Especifica a ID de uma coleção de configurações HTTP de back-end existente que pode ser adicionada às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="00bd5-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00bd5-141">As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="00bd5-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="00bd5-142">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="00bd5-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="00bd5-143">Por exemplo:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" as configurações HTTP de back-end configurar propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="00bd5-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="00bd5-144">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="00bd5-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="00bd5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bd5-145">-DefaultProfile</span></span>
<span data-ttu-id="00bd5-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00bd5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00bd5-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="00bd5-147">-Name</span></span>
<span data-ttu-id="00bd5-148">Especifica o nome da configuração de regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="00bd5-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="00bd5-149">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="00bd5-149">-Paths</span></span>
<span data-ttu-id="00bd5-150">Especifica uma ou mais regras de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="00bd5-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="00bd5-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00bd5-151">-RedirectConfiguration</span></span>
<span data-ttu-id="00bd5-152">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="00bd5-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="00bd5-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="00bd5-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="00bd5-154">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00bd5-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="00bd5-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00bd5-155">-RewriteRuleSet</span></span>
<span data-ttu-id="00bd5-156">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="00bd5-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="00bd5-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="00bd5-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="00bd5-158">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="00bd5-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="00bd5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bd5-159">CommonParameters</span></span>
<span data-ttu-id="00bd5-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bd5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bd5-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bd5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bd5-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00bd5-162">INPUTS</span></span>

### <span data-ttu-id="00bd5-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="00bd5-163">None</span></span>

## <span data-ttu-id="00bd5-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00bd5-164">OUTPUTS</span></span>

### <span data-ttu-id="00bd5-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="00bd5-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="00bd5-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00bd5-166">NOTES</span></span>

## <span data-ttu-id="00bd5-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00bd5-167">RELATED LINKS</span></span>

[<span data-ttu-id="00bd5-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00bd5-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00bd5-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="00bd5-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00bd5-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00bd5-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="00bd5-172">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00bd5-172">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="00bd5-173">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-173">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="00bd5-174">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-174">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00bd5-175">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-175">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00bd5-176">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00bd5-176">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


