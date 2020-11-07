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
# <span data-ttu-id="75d16-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="75d16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75d16-102">SYNOPSIS</span></span>
<span data-ttu-id="75d16-103">Cria uma regra de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d16-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="75d16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75d16-104">SYNTAX</span></span>

### <span data-ttu-id="75d16-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="75d16-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d16-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="75d16-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75d16-107">DESCRIPTION</span></span>
<span data-ttu-id="75d16-108">O cmdlet **New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d16-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="75d16-109">Regras criadas por este cmdlet podem ser adicionadas a uma coleção de definições de configuração do mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="75d16-110">As definições de configuração do mapa de caminho são usadas no balanceamento de carga do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="75d16-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75d16-111">EXAMPLES</span></span>

### <span data-ttu-id="75d16-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75d16-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="75d16-113">Esses comandos criam uma nova regra de caminho do gateway do aplicativo e, em seguida, usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d16-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="75d16-114">Para fazer isso, o primeiro comando cria uma referência de objeto para o ContosoApplicationGateway do gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="75d16-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="75d16-116">Os próximos dois comandos criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="75d16-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="75d16-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="75d16-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="75d16-118">O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as definições de configuração e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="75d16-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="75d16-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="75d16-120">Esse comando cria uma regra de caminho com o nome "base", trajetórias como "/base", BackendAddressPool como $AddressPool, BackendHttpSettings como $HttpSettings e FirewallPolicy como $firewallPolicy. NGS e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="75d16-121">OS</span><span class="sxs-lookup"><span data-stu-id="75d16-121">PARAMETERS</span></span>

### <span data-ttu-id="75d16-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="75d16-122">-BackendAddressPool</span></span>
<span data-ttu-id="75d16-123">Especifica uma referência de objeto a um conjunto de configurações do pool de endereços back-end a serem adicionadas às configurações de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="75d16-124">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhante a esta: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="75d16-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="75d16-125">O comando anterior adiciona dois endereços de IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="75d16-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="75d16-126">Observe que o endereço IP fica entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="75d16-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="75d16-127">A variável resultante, $AddressPool, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="75d16-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="75d16-128">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="75d16-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="75d16-129">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="75d16-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="75d16-130">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="75d16-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="75d16-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="75d16-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="75d16-132">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="75d16-133">As IDs de pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="75d16-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="75d16-134">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="75d16-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="75d16-135">Por exemplo:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" o pool de endereços de back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="75d16-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="75d16-136">Esses endereços IP devem pertencer à sub-rede da rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="75d16-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="75d16-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="75d16-137">-BackendHttpSettings</span></span>
<span data-ttu-id="75d16-138">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="75d16-139">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSettings e a sintaxe semelhante a esta: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled" a variável resultante, $HttpSettings, pode ser usada como o valor do parâmetro para o parâmetro *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings as configurações http de back-end configuram propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="75d16-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="75d16-140">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="75d16-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="75d16-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="75d16-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="75d16-142">Especifica a ID de uma coleção de configurações HTTP de back-end existente que pode ser adicionada às definições de configuração de regra de caminho de gateway.</span><span class="sxs-lookup"><span data-stu-id="75d16-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="75d16-143">As IDs de configuração HTTP podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="75d16-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="75d16-144">Depois de ter a ID, você pode usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="75d16-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="75d16-145">Por exemplo:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" as configurações HTTP de back-end configurar propriedades como porta, protocolo e afinidade baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="75d16-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="75d16-146">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="75d16-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="75d16-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="75d16-147">-FirewallPolicy</span></span>
<span data-ttu-id="75d16-148">Especifica a referência de objeto a uma política de firewall de nível superior.</span><span class="sxs-lookup"><span data-stu-id="75d16-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="75d16-149">A referência do objeto pode ser criada usando-se New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75d16-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="75d16-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-The Resource "rgName" uma política de firewall criada usando o commandlet acima pode ser referida em um nível de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="75d16-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="75d16-151">o comando acima criaria as configurações de política padrão e as regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="75d16-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="75d16-152">Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="75d16-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d16-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="75d16-153">-FirewallPolicyId</span></span>
<span data-ttu-id="75d16-154">Especifica a ID de um recurso existente de firewall de aplicativo Web de nível superior.</span><span class="sxs-lookup"><span data-stu-id="75d16-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="75d16-155">IDs de política de firewall podem ser retornadas usando o cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="75d16-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="75d16-156">Depois que tivermos a ID, você poderá usar o parâmetro *FirewallPolicyId* em vez do parâmetro *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="75d16-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="75d16-157">Por exemplo:-FirewallPolicyId "/subscriptions/<assinatura-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="75d16-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d16-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d16-158">-DefaultProfile</span></span>
<span data-ttu-id="75d16-159">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75d16-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d16-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="75d16-160">-Name</span></span>
<span data-ttu-id="75d16-161">Especifica o nome da configuração de regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="75d16-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="75d16-162">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="75d16-162">-Paths</span></span>
<span data-ttu-id="75d16-163">Especifica uma ou mais regras de caminho do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75d16-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="75d16-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="75d16-164">-RedirectConfiguration</span></span>
<span data-ttu-id="75d16-165">RedirectConfiguration do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="75d16-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="75d16-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="75d16-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="75d16-167">ID do aplicativo do gateway de RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="75d16-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="75d16-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75d16-168">-RewriteRuleSet</span></span>
<span data-ttu-id="75d16-169">RewriteRuleSet do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="75d16-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="75d16-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="75d16-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="75d16-171">ID do aplicativo do gateway de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="75d16-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="75d16-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d16-172">CommonParameters</span></span>
<span data-ttu-id="75d16-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d16-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d16-174">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d16-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d16-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75d16-175">INPUTS</span></span>

### <span data-ttu-id="75d16-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75d16-176">None</span></span>

## <span data-ttu-id="75d16-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75d16-177">OUTPUTS</span></span>

### <span data-ttu-id="75d16-178">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="75d16-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="75d16-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75d16-179">NOTES</span></span>

## <span data-ttu-id="75d16-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75d16-180">RELATED LINKS</span></span>

[<span data-ttu-id="75d16-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="75d16-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75d16-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="75d16-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="75d16-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="75d16-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="75d16-185">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="75d16-185">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="75d16-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="75d16-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="75d16-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="75d16-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="75d16-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


