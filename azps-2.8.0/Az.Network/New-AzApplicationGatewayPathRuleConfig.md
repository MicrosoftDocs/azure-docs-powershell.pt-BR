---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 6592f79291c069ade40b30277461f5e0e218b937
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407039"
---
# <span data-ttu-id="26db1-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="26db1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26db1-102">SYNOPSIS</span></span>
<span data-ttu-id="26db1-103">Cria uma regra de caminho do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26db1-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="26db1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26db1-104">SYNTAX</span></span>

### <span data-ttu-id="26db1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26db1-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26db1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26db1-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26db1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="26db1-107">DESCRIPTION</span></span>
<span data-ttu-id="26db1-108">O **cmdlet New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26db1-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="26db1-109">As regras criadas por esse cmdlet podem ser adicionadas a um conjunto de configurações de mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="26db1-110">As configurações de configuração de mapa de caminho são usadas no balanceamento de carga do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26db1-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="26db1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="26db1-111">EXAMPLES</span></span>

### <span data-ttu-id="26db1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26db1-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="26db1-113">Esses comandos criam uma nova regra de caminho do gateway de aplicativo e usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26db1-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="26db1-114">Para fazer isso, o primeiro comando cria uma referência de objeto ao gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="26db1-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="26db1-116">Os dois comandos a seguir criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="26db1-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="26db1-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="26db1-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="26db1-118">O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as configurações e a nova regra de caminho contida nessas configurações ao ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="26db1-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26db1-119">PARAMETERS</span></span>

### <span data-ttu-id="26db1-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="26db1-120">-BackendAddressPool</span></span>
<span data-ttu-id="26db1-121">Especifica uma referência de objeto a um conjunto de configurações de pool de endereços de back-end a serem adicionadas às configurações de configuração de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="26db1-122">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhantes a esta: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="26db1-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="26db1-123">O comando anterior adiciona dois endereços IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="26db1-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="26db1-124">Observe que o endereço IP está entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="26db1-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="26db1-125">A variável resultante, $AddressPool, pode ser usada como o valor de parâmetro para o parâmetro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="26db1-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="26db1-126">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26db1-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="26db1-127">Esses endereços IP devem pertencer à sub-rede de rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="26db1-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="26db1-128">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="26db1-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="26db1-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="26db1-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="26db1-130">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="26db1-131">As IDs do pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool endereço.</span><span class="sxs-lookup"><span data-stu-id="26db1-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="26db1-132">Depois de ter a ID, você poderá usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="26db1-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="26db1-133">Por exemplo: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="26db1-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="26db1-134">Esses endereços IP devem pertencer à sub-rede de rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="26db1-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="26db1-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="26db1-135">-BackendHttpSettings</span></span>
<span data-ttu-id="26db1-136">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="26db1-137">Você pode criar esta referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSettings e a sintaxe semelhantes a esta: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" (Desabilitado) a variável resultante, $HttpSettings, pode ser usado como o valor de parâmetro para o parâmetro *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings As configurações HTTP de back-end configuram propriedades como porta, protocolo e affinity baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="26db1-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="26db1-138">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="26db1-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="26db1-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="26db1-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="26db1-140">Especifica a ID de um conjunto de configurações HTTP back-end existente que pode ser adicionado às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="26db1-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="26db1-141">As IDs de configuração HTTP podem ser retornadas usando Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26db1-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="26db1-142">Depois de ter a ID, você poderá usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="26db1-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="26db1-143">Por exemplo: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" As configurações http back-end configuram propriedades como porta, protocolo, e affinity baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="26db1-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="26db1-144">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="26db1-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="26db1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26db1-145">-DefaultProfile</span></span>
<span data-ttu-id="26db1-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="26db1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26db1-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="26db1-147">-Name</span></span>
<span data-ttu-id="26db1-148">Especifica o nome da configuração da regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="26db1-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="26db1-149">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="26db1-149">-Paths</span></span>
<span data-ttu-id="26db1-150">Especifica uma ou mais regras de caminho do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="26db1-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="26db1-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26db1-151">-RedirectConfiguration</span></span>
<span data-ttu-id="26db1-152">RedirectConfiguration do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="26db1-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="26db1-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26db1-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="26db1-154">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26db1-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="26db1-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26db1-155">-RewriteRuleSet</span></span>
<span data-ttu-id="26db1-156">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26db1-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="26db1-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="26db1-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="26db1-158">ID do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26db1-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="26db1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26db1-159">CommonParameters</span></span>
<span data-ttu-id="26db1-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26db1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26db1-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26db1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26db1-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="26db1-162">INPUTS</span></span>

### <span data-ttu-id="26db1-163">Nenhum</span><span class="sxs-lookup"><span data-stu-id="26db1-163">None</span></span>

## <span data-ttu-id="26db1-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="26db1-164">OUTPUTS</span></span>

### <span data-ttu-id="26db1-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="26db1-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="26db1-166">Notas</span><span class="sxs-lookup"><span data-stu-id="26db1-166">NOTES</span></span>

## <span data-ttu-id="26db1-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26db1-167">RELATED LINKS</span></span>

[<span data-ttu-id="26db1-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26db1-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26db1-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="26db1-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26db1-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="26db1-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="26db1-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="26db1-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26db1-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26db1-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26db1-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


