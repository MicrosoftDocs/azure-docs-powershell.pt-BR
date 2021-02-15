---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f06dbac5e7c7a67acc38c5357351905fab0ed141
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402551"
---
# <span data-ttu-id="c1051-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="c1051-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1051-102">SYNOPSIS</span></span>
<span data-ttu-id="c1051-103">Cria uma regra de caminho do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1051-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="c1051-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1051-104">SYNTAX</span></span>

### <span data-ttu-id="c1051-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1051-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1051-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1051-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1051-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1051-107">DESCRIPTION</span></span>
<span data-ttu-id="c1051-108">O **cmdlet New-AzApplicationGatewayPathRuleConfig** cria uma regra de caminho de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1051-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="c1051-109">As regras criadas por esse cmdlet podem ser adicionadas a um conjunto de configurações de mapa de caminho de URL e atribuídas a um gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="c1051-110">As configurações de configuração de mapa de caminho são usadas no balanceamento de carga do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1051-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="c1051-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1051-111">EXAMPLES</span></span>

### <span data-ttu-id="c1051-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1051-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="c1051-113">Esses comandos criam uma nova regra de caminho do gateway de aplicativo e usam o cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** para atribuir essa regra a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1051-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="c1051-114">Para fazer isso, o primeiro comando cria uma referência de objeto ao gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="c1051-115">Essa referência de objeto é armazenada em uma variável chamada $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="c1051-116">Os dois comandos a seguir criam um pool de endereços back-end e um objeto de configurações HTTP back-end; esses objetos (armazenados nas variáveis $AddressPool e $HttpSettings) são necessários para criar um objeto de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="c1051-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="c1051-117">O quarto comando cria o objeto de regra de caminho e é armazenado em uma variável chamada $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="c1051-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="c1051-118">O quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** para adicionar as configurações e a nova regra de caminho contida nessas configurações ao ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="c1051-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c1051-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="c1051-120">Esse comando cria uma regra de caminho com o Nome como "base", Caminhos como "/base", BackendAddressPool como $AddressPool, BackendHttpSettings como $HttpSettings e FirewallPolicy como $firewallPolicy.ngs e a nova regra de caminho contida nessas configurações para ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="c1051-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1051-121">PARAMETERS</span></span>

### <span data-ttu-id="c1051-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1051-122">-BackendAddressPool</span></span>
<span data-ttu-id="c1051-123">Especifica uma referência de objeto a um conjunto de configurações de pool de endereços de back-end a serem adicionadas às configurações de configuração de regras de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="c1051-124">Você pode criar essa referência de objeto usando o cmdlet New-AzApplicationGatewayBackendAddressPool e a sintaxe semelhantes a esta: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="c1051-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="c1051-125">O comando anterior adiciona dois endereços IP (192.16.1.1 e 192.168.1.2) ao pool de endereços.</span><span class="sxs-lookup"><span data-stu-id="c1051-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="c1051-126">Observe que o endereço IP está entre aspas e separado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c1051-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="c1051-127">A variável resultante, $AddressPool, pode ser usada como o valor de parâmetro para o parâmetro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="c1051-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c1051-128">O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="c1051-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c1051-129">Esses endereços IP devem pertencer à sub-rede de rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="c1051-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="c1051-130">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendAddressPoolId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="c1051-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1051-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c1051-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="c1051-132">Especifica a ID de um pool de endereços back-end existente que pode ser adicionado às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1051-133">As IDs do pool de endereços podem ser retornadas usando o cmdlet Get-AzApplicationGatewayBackendAddressPool endereço.</span><span class="sxs-lookup"><span data-stu-id="c1051-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="c1051-134">Depois de ter a ID, você poderá usar o parâmetro *DefaultBackendAddressPoolId* em vez do parâmetro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="c1051-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c1051-135">Por exemplo: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" O pool de endereços back-end representa os endereços IP nos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="c1051-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c1051-136">Esses endereços IP devem pertencer à sub-rede de rede virtual ou devem ser endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="c1051-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="c1051-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1051-137">-BackendHttpSettings</span></span>
<span data-ttu-id="c1051-138">Especifica uma referência de objeto a um conjunto de configurações HTTP de back-end a serem adicionadas às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1051-139">Você pode criar esta referência de objeto usando o cmdlet New-AzApplicationGatewayBackendHttpSettings e a sintaxe semelhantes a esta: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" (Desabilitado) a variável resultante, $HttpSettings, pode ser usado como o valor de parâmetro para o parâmetro *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings As configurações HTTP de back-end configuram propriedades como porta, protocolo e affinity baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="c1051-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c1051-140">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettingsId* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="c1051-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1051-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c1051-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c1051-142">Especifica a ID de um conjunto de configurações HTTP back-end existente que pode ser adicionado às configurações de configuração da regra de caminho do gateway.</span><span class="sxs-lookup"><span data-stu-id="c1051-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1051-143">As IDs de configuração HTTP podem ser retornadas usando Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1051-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="c1051-144">Depois de ter a ID, você poderá usar o parâmetro *DefaultBackendHttpSettingsId* em vez do parâmetro *DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="c1051-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="c1051-145">Por exemplo: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" As configurações http de back-end configuram propriedades como porta, protocolo, e affinity baseada em cookies para um pool de back-end.</span><span class="sxs-lookup"><span data-stu-id="c1051-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c1051-146">Se você usar esse parâmetro, não poderá usar o parâmetro *DefaultBackendHttpSettings* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="c1051-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1051-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c1051-147">-FirewallPolicy</span></span>
<span data-ttu-id="c1051-148">Especifica a referência de objeto a uma política de firewall de nível superior.</span><span class="sxs-lookup"><span data-stu-id="c1051-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="c1051-149">A referência de objeto pode ser criada usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1051-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="c1051-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Uma política de firewall criada usando o commandlet acima pode ser referenciada em um nível de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="c1051-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="c1051-151">ele acima do comando criaria uma configuração de política padrão e regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="c1051-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="c1051-152">Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c1051-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1051-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c1051-153">-FirewallPolicyId</span></span>
<span data-ttu-id="c1051-154">Especifica a ID de um recurso de firewall de aplicativo Web de nível superior existente.</span><span class="sxs-lookup"><span data-stu-id="c1051-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="c1051-155">As IDs de política de firewall podem ser retornadas usando Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1051-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="c1051-156">Depois de termos a ID, você pode usar o *parâmetro FirewallPolicyId em* vez do *parâmetro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="c1051-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="c1051-157">Por exemplo: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="c1051-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1051-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1051-158">-DefaultProfile</span></span>
<span data-ttu-id="c1051-159">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c1051-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1051-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1051-160">-Name</span></span>
<span data-ttu-id="c1051-161">Especifica o nome da configuração da regra de caminho que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c1051-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c1051-162">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="c1051-162">-Paths</span></span>
<span data-ttu-id="c1051-163">Especifica uma ou mais regras de caminho do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1051-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="c1051-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1051-164">-RedirectConfiguration</span></span>
<span data-ttu-id="c1051-165">RedirectConfiguration do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="c1051-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1051-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c1051-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="c1051-167">ID do gateway de aplicativo RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1051-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1051-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1051-168">-RewriteRuleSet</span></span>
<span data-ttu-id="c1051-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1051-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1051-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c1051-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="c1051-171">ID do gateway de aplicativo RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1051-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1051-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1051-172">CommonParameters</span></span>
<span data-ttu-id="c1051-173">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1051-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1051-174">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1051-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1051-175">Entradas</span><span class="sxs-lookup"><span data-stu-id="c1051-175">INPUTS</span></span>

### <span data-ttu-id="c1051-176">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c1051-176">None</span></span>

## <span data-ttu-id="c1051-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="c1051-177">OUTPUTS</span></span>

### <span data-ttu-id="c1051-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="c1051-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="c1051-179">Notas</span><span class="sxs-lookup"><span data-stu-id="c1051-179">NOTES</span></span>

## <span data-ttu-id="c1051-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1051-180">RELATED LINKS</span></span>

[<span data-ttu-id="c1051-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1051-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1051-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c1051-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1051-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1051-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="c1051-185">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-185">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="c1051-186">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-186">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1051-187">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-187">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1051-188">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1051-188">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


