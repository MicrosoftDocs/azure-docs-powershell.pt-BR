---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a9ec7589ab155553da29612096a607d82a078321
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85267809"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="fda78-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fda78-103">Azure PowerShell release notes</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="fda78-104">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-104">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-105">Az.Accounts</span></span>
* <span data-ttu-id="fda78-106">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="fda78-106">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="fda78-107">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="fda78-107">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="fda78-108">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="fda78-108">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="fda78-109">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="fda78-109">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="fda78-110">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fda78-110">Az.Aks</span></span>
* <span data-ttu-id="fda78-111">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="fda78-111">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-112">Az.Batch</span></span>
* <span data-ttu-id="fda78-113">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="fda78-113">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="fda78-114">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-114">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-115">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-115">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-116">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="fda78-116">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="fda78-117">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="fda78-117">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-118">Az.Compute</span></span>
* <span data-ttu-id="fda78-119">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="fda78-119">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="fda78-120">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="fda78-120">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="fda78-121">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="fda78-121">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="fda78-122">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="fda78-122">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="fda78-123">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="fda78-123">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-124">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-125">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="fda78-125">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-126">Az.EventHub</span></span>
* <span data-ttu-id="fda78-127">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="fda78-127">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="fda78-128">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="fda78-128">Az.Functions</span></span>
* <span data-ttu-id="fda78-129">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="fda78-129">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-130">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-131">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fda78-131">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fda78-132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fda78-132">Az.HealthcareApis</span></span>
* <span data-ttu-id="fda78-133">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="fda78-133">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="fda78-134">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="fda78-134">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-135">Az.Monitor</span></span>
* <span data-ttu-id="fda78-136">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="fda78-136">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="fda78-137">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="fda78-137">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-138">Az.Network</span></span>
* <span data-ttu-id="fda78-139">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="fda78-139">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="fda78-140">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-140">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="fda78-141">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="fda78-141">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="fda78-142">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="fda78-142">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="fda78-143">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="fda78-143">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="fda78-144">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="fda78-144">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="fda78-145">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="fda78-145">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="fda78-146">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="fda78-146">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="fda78-147">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="fda78-147">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="fda78-148">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="fda78-148">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="fda78-149">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-149">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="fda78-150">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-150">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="fda78-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="fda78-151">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="fda78-152">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-152">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="fda78-153">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="fda78-153">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="fda78-154">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="fda78-154">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="fda78-155">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="fda78-155">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="fda78-156">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-156">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="fda78-157">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="fda78-157">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="fda78-158">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="fda78-158">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="fda78-159">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="fda78-159">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="fda78-160">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="fda78-160">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="fda78-161">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="fda78-161">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="fda78-162">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="fda78-162">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="fda78-163">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fda78-163">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="fda78-164">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="fda78-164">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="fda78-165">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="fda78-165">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="fda78-166">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fda78-166">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="fda78-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-167">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="fda78-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-168">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="fda78-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-169">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="fda78-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-170">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="fda78-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-171">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="fda78-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-172">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="fda78-173">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fda78-173">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="fda78-174">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="fda78-174">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="fda78-175">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-175">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="fda78-176">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-176">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="fda78-177">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-177">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="fda78-178">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-178">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="fda78-179">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="fda78-179">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="fda78-180">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-180">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="fda78-181">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-181">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="fda78-182">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-182">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="fda78-183">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-183">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="fda78-184">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-184">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="fda78-185">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-185">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="fda78-186">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-186">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="fda78-187">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-187">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-188">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-188">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-189">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="fda78-189">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="fda78-190">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="fda78-190">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="fda78-191">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="fda78-191">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="fda78-192">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="fda78-192">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="fda78-193">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="fda78-193">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-194">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-194">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-195">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-195">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="fda78-196">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="fda78-196">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-197">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-197">Az.Resources</span></span>
* <span data-ttu-id="fda78-198">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="fda78-198">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="fda78-199">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="fda78-199">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="fda78-200">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="fda78-200">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="fda78-201">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-201">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="fda78-202">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="fda78-202">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="fda78-203">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="fda78-203">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-204">Az.Sql</span></span>
* <span data-ttu-id="fda78-205">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="fda78-205">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="fda78-206">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="fda78-206">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="fda78-207">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="fda78-207">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-208">Az.Storage</span></span>
* <span data-ttu-id="fda78-209">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="fda78-209">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="fda78-210">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-210">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="fda78-211">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-211">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-212">Az.Websites</span></span>
* <span data-ttu-id="fda78-213">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="fda78-213">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fda78-214">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="fda78-214">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="fda78-215">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="fda78-215">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="fda78-216">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fda78-216">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="fda78-217">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="fda78-217">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="fda78-218">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="fda78-218">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="fda78-219">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-219">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-220">Az.Accounts</span></span>
* <span data-ttu-id="fda78-221">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="fda78-221">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fda78-222">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fda78-222">Az.AnalysisServices</span></span>
* <span data-ttu-id="fda78-223">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-223">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-224">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-224">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-225">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-225">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="fda78-226">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fda78-226">Az.Billing</span></span>
* <span data-ttu-id="fda78-227">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-227">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-228">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-229">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="fda78-229">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-230">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-231">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-231">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="fda78-232">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="fda78-232">Az.DataShare</span></span>
* <span data-ttu-id="fda78-233">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="fda78-233">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="fda78-234">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="fda78-234">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="fda78-235">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="fda78-235">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-236">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-236">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-237">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="fda78-237">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="fda78-238">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="fda78-238">Added optional parameters to</span></span> 
    - <span data-ttu-id="fda78-239">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="fda78-239">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="fda78-240">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="fda78-240">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-241">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-241">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-242">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="fda78-242">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="fda78-243">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fda78-243">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="fda78-244">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-244">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="fda78-245">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="fda78-245">Az.PrivateDns</span></span>
* <span data-ttu-id="fda78-246">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fda78-246">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-248">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="fda78-248">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="fda78-249">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fda78-249">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-250">Az.Resources</span></span>
* <span data-ttu-id="fda78-251">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="fda78-251">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="fda78-252">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="fda78-252">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="fda78-253">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="fda78-253">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="fda78-254">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda78-254">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="fda78-255">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-255">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-256">Az.Sql</span></span>
* <span data-ttu-id="fda78-257">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="fda78-257">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="fda78-258">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="fda78-258">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="fda78-259">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="fda78-259">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-260">Az.Storage</span></span>
* <span data-ttu-id="fda78-261">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-261">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="fda78-262">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-262">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="fda78-263">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="fda78-263">Highlights since the last release</span></span>
* <span data-ttu-id="fda78-264">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="fda78-264">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="fda78-265">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="fda78-265">General availability of Az.Functions</span></span> 
* <span data-ttu-id="fda78-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-266">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-267">Az.Accounts</span></span>
* <span data-ttu-id="fda78-268">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="fda78-268">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="fda78-269">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="fda78-269">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="fda78-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fda78-270">Az.Aks</span></span>
* <span data-ttu-id="fda78-271">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="fda78-271">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="fda78-272">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="fda78-272">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="fda78-273">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="fda78-273">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-274">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-275">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="fda78-275">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="fda78-276">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="fda78-276">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="fda78-277">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="fda78-277">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="fda78-278">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="fda78-278">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="fda78-279">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="fda78-279">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="fda78-280">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="fda78-280">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="fda78-281">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="fda78-281">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="fda78-282">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="fda78-282">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="fda78-283">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="fda78-283">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="fda78-284">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="fda78-284">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="fda78-285">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="fda78-285">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="fda78-286">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="fda78-286">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="fda78-287">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="fda78-287">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="fda78-288">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="fda78-288">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="fda78-289">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="fda78-289">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="fda78-290">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="fda78-290">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="fda78-291">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-291">Az.ApplicationInsights</span></span>
* <span data-ttu-id="fda78-292">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="fda78-292">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="fda78-293">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="fda78-293">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="fda78-294">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="fda78-294">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-295">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-295">Az.Batch</span></span>
* <span data-ttu-id="fda78-296">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="fda78-296">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="fda78-297">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="fda78-297">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="fda78-298">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="fda78-298">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="fda78-299">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="fda78-299">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="fda78-300">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="fda78-300">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="fda78-301">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="fda78-301">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="fda78-302">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="fda78-302">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="fda78-303">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="fda78-303">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="fda78-304">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="fda78-304">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-305">Az.Compute</span></span>
* <span data-ttu-id="fda78-306">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="fda78-306">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="fda78-307">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="fda78-307">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="fda78-308">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="fda78-308">Breaking changes</span></span>
    - <span data-ttu-id="fda78-309">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="fda78-309">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="fda78-310">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="fda78-310">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="fda78-311">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="fda78-311">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="fda78-312">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="fda78-312">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="fda78-313">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="fda78-313">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="fda78-314">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="fda78-314">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="fda78-315">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="fda78-315">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-316">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-316">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-317">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fda78-317">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-318">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-319">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="fda78-319">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="fda78-320">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="fda78-320">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="fda78-321">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="fda78-321">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="fda78-322">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="fda78-322">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="fda78-323">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="fda78-323">Az.Functions</span></span>
* <span data-ttu-id="fda78-324">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="fda78-324">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-325">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-325">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-326">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="fda78-326">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fda78-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fda78-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="fda78-328">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="fda78-328">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-329">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-329">Az.IotHub</span></span>
* <span data-ttu-id="fda78-330">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="fda78-330">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="fda78-331">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="fda78-331">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="fda78-332">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="fda78-332">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="fda78-333">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="fda78-333">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="fda78-334">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="fda78-334">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="fda78-335">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-335">New cmdlets are:</span></span>
    - <span data-ttu-id="fda78-336">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-336">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="fda78-337">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-337">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="fda78-338">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-338">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="fda78-339">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-339">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="fda78-340">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="fda78-340">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="fda78-341">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="fda78-341">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-342">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-342">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-343">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="fda78-343">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="fda78-344">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fda78-344">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="fda78-345">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="fda78-345">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="fda78-346">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="fda78-346">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="fda78-347">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="fda78-347">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="fda78-348">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="fda78-348">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="fda78-349">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="fda78-349">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-350">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-350">Az.Monitor</span></span>
* <span data-ttu-id="fda78-351">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="fda78-351">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="fda78-352">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="fda78-352">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="fda78-353">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="fda78-353">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="fda78-354">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="fda78-354">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="fda78-355">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="fda78-355">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="fda78-356">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="fda78-356">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="fda78-357">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="fda78-357">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-358">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-358">Az.Network</span></span>
* <span data-ttu-id="fda78-359">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="fda78-359">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="fda78-360">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="fda78-360">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="fda78-361">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="fda78-361">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="fda78-362">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="fda78-362">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="fda78-363">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fda78-363">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="fda78-364">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-364">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-365">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fda78-365">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="fda78-366">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fda78-366">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="fda78-367">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fda78-367">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="fda78-368">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fda78-368">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="fda78-369">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-369">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="fda78-370">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="fda78-370">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="fda78-371">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="fda78-371">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="fda78-372">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="fda78-372">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="fda78-373">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="fda78-373">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="fda78-374">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="fda78-374">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="fda78-375">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="fda78-375">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="fda78-376">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-376">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="fda78-377">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-377">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="fda78-378">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-378">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="fda78-379">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-379">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="fda78-380">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="fda78-380">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="fda78-381">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="fda78-381">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="fda78-382">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-382">Updated cmdlet:</span></span>
        - <span data-ttu-id="fda78-383">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fda78-383">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-384">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-384">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-385">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="fda78-385">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="fda78-386">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="fda78-386">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="fda78-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="fda78-387">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="fda78-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="fda78-388">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="fda78-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="fda78-389">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="fda78-390">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="fda78-390">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="fda78-391">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="fda78-391">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="fda78-392">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="fda78-392">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-393">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-393">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-394">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-394">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="fda78-395">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="fda78-395">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="fda78-396">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="fda78-396">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="fda78-397">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="fda78-397">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="fda78-398">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="fda78-398">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-399">Az.Resources</span></span>
* <span data-ttu-id="fda78-400">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="fda78-400">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="fda78-401">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="fda78-401">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="fda78-402">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="fda78-402">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="fda78-403">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="fda78-403">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="fda78-404">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="fda78-404">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="fda78-405">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="fda78-405">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="fda78-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="fda78-406">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="fda78-407">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="fda78-407">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="fda78-408">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="fda78-408">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="fda78-409">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="fda78-409">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="fda78-410">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="fda78-410">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="fda78-411">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="fda78-411">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="fda78-412">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="fda78-412">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="fda78-413">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="fda78-413">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="fda78-414">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="fda78-414">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="fda78-415">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="fda78-415">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="fda78-416">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-416">'New-AzDeployment'</span></span>
    - <span data-ttu-id="fda78-417">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-417">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="fda78-418">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-418">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="fda78-419">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-419">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-421">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="fda78-421">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-422">Az.Sql</span></span>
* <span data-ttu-id="fda78-423">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="fda78-423">Enhance performance of:</span></span>
    - <span data-ttu-id="fda78-424">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="fda78-424">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="fda78-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="fda78-425">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="fda78-426">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="fda78-426">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="fda78-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="fda78-427">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="fda78-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="fda78-428">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="fda78-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="fda78-429">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="fda78-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="fda78-430">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="fda78-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="fda78-431">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="fda78-432">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="fda78-432">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="fda78-433">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="fda78-433">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-434">Az.Storage</span></span>
* <span data-ttu-id="fda78-435">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-435">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="fda78-436">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="fda78-436">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="fda78-437">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-437">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="fda78-438">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="fda78-438">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="fda78-439">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="fda78-439">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="fda78-440">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="fda78-440">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="fda78-441">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-441">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="fda78-442">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-442">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="fda78-443">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="fda78-443">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="fda78-444">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="fda78-444">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="fda78-445">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="fda78-445">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="fda78-446">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="fda78-446">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="fda78-447">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="fda78-447">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="fda78-448">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-448">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="fda78-449">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-449">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="fda78-450">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-450">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="fda78-451">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-451">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="fda78-452">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="fda78-452">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="fda78-453">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="fda78-453">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="fda78-454">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="fda78-454">Supported failover Storage account</span></span>
    - <span data-ttu-id="fda78-455">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="fda78-455">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="fda78-456">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-456">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="fda78-457">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-457">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="fda78-458">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="fda78-458">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="fda78-459">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="fda78-459">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="fda78-460">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="fda78-460">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="fda78-461">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="fda78-461">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="fda78-462">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="fda78-462">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="fda78-463">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="fda78-463">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="fda78-464">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="fda78-464">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="fda78-465">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="fda78-465">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="fda78-466">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="fda78-466">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="fda78-467">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="fda78-467">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="fda78-468">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="fda78-468">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="fda78-469">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="fda78-469">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="fda78-470">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="fda78-470">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="fda78-471">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="fda78-471">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="fda78-472">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="fda78-472">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="fda78-473">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="fda78-473">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="fda78-474">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fda78-474">Az.TrafficManager</span></span>
* <span data-ttu-id="fda78-475">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="fda78-475">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-476">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-476">Az.Websites</span></span>
* <span data-ttu-id="fda78-477">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="fda78-477">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="fda78-478">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-478">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="fda78-479">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="fda78-479">Highlights since the last release</span></span>
* <span data-ttu-id="fda78-480">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="fda78-480">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-481">Az.Accounts</span></span>
* <span data-ttu-id="fda78-482">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="fda78-482">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-483">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-483">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-484">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="fda78-484">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="fda78-485">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="fda78-485">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-486">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-486">Az.Cdn</span></span>
* <span data-ttu-id="fda78-487">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="fda78-487">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-488">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-489">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="fda78-489">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-490">Az.Compute</span></span>
* <span data-ttu-id="fda78-491">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="fda78-491">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="fda78-492">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="fda78-492">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-493">Az.IotHub</span></span>
* <span data-ttu-id="fda78-494">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-494">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="fda78-495">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="fda78-495">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="fda78-496">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="fda78-496">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="fda78-497">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="fda78-497">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="fda78-498">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-498">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="fda78-499">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="fda78-499">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="fda78-500">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="fda78-500">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="fda78-501">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="fda78-501">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="fda78-502">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-502">New cmdlets are:</span></span>
    - <span data-ttu-id="fda78-503">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-503">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="fda78-504">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-504">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="fda78-505">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-505">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="fda78-506">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-506">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="fda78-507">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="fda78-507">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-508">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-509">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="fda78-509">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="fda78-510">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="fda78-510">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="fda78-511">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="fda78-511">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="fda78-512">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="fda78-512">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="fda78-513">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="fda78-513">Az.Maintenance</span></span>
* <span data-ttu-id="fda78-514">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="fda78-514">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-515">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-515">Az.Monitor</span></span>
* <span data-ttu-id="fda78-516">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="fda78-516">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="fda78-517">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="fda78-517">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="fda78-518">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="fda78-518">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="fda78-519">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="fda78-519">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="fda78-520">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="fda78-520">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="fda78-521">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="fda78-521">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="fda78-522">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="fda78-522">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="fda78-523">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="fda78-523">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-524">Az.Network</span></span>
* <span data-ttu-id="fda78-525">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="fda78-525">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="fda78-526">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-526">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="fda78-527">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-527">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="fda78-528">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-528">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="fda78-529">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-529">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="fda78-530">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="fda78-530">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="fda78-531">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-531">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="fda78-532">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="fda78-532">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="fda78-533">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="fda78-533">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="fda78-534">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-534">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="fda78-535">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="fda78-535">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="fda78-536">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="fda78-536">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="fda78-537">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="fda78-537">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="fda78-538">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="fda78-538">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="fda78-539">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-539">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="fda78-540">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-540">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-541">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-541">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-542">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="fda78-542">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="fda78-543">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="fda78-543">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-544">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-545">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="fda78-545">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-546">Az.Sql</span></span>
* <span data-ttu-id="fda78-547">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-547">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="fda78-548">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="fda78-548">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-549">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-549">Az.Storage</span></span>
* <span data-ttu-id="fda78-550">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="fda78-550">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="fda78-551">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-551">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="fda78-552">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-552">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="fda78-553">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-553">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="fda78-554">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="fda78-554">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="fda78-555">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="fda78-555">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="fda78-556">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="fda78-556">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="fda78-557">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="fda78-557">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="fda78-558">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="fda78-558">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="fda78-559">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="fda78-559">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="fda78-560">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="fda78-560">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="fda78-561">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="fda78-561">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="fda78-562">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="fda78-562">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="fda78-563">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-563">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="fda78-564">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-564">General</span></span>
* <span data-ttu-id="fda78-565">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="fda78-565">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="fda78-566">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="fda78-566">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="fda78-567">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="fda78-567">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="fda78-568">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="fda78-568">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="fda78-569">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fda78-569">Az.Billing</span></span>
  - <span data-ttu-id="fda78-570">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-570">Az.Compute</span></span>
  - <span data-ttu-id="fda78-571">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="fda78-571">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="fda78-572">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-572">Az.EventHub</span></span>
  - <span data-ttu-id="fda78-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-573">Az.IotHub</span></span>
  - <span data-ttu-id="fda78-574">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-574">Az.KeyVault</span></span>
  - <span data-ttu-id="fda78-575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-575">Az.Monitor</span></span>
  - <span data-ttu-id="fda78-576">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-576">Az.Network</span></span>
  - <span data-ttu-id="fda78-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-577">Az.Resources</span></span>
  - <span data-ttu-id="fda78-578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-578">Az.Storage</span></span>
  - <span data-ttu-id="fda78-579">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-579">Az.Websites</span></span>
* <span data-ttu-id="fda78-580">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-580">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="fda78-581">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="fda78-581">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="fda78-582">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="fda78-582">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="fda78-583">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-583">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-584">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-584">Az.Accounts</span></span>
* <span data-ttu-id="fda78-585">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="fda78-585">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-586">Az.Compute</span></span>
* <span data-ttu-id="fda78-587">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="fda78-587">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="fda78-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="fda78-588">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="fda78-589">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="fda78-589">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="fda78-590">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="fda78-590">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="fda78-591">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="fda78-591">[#11354]</span></span>
* <span data-ttu-id="fda78-592">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="fda78-592">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="fda78-593">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="fda78-593">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="fda78-594">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="fda78-594">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="fda78-595">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="fda78-595">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="fda78-596">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="fda78-596">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="fda78-597">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-597">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="fda78-598">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="fda78-598">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="fda78-599">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fda78-599">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="fda78-600">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="fda78-600">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-601">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-602">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="fda78-602">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="fda78-603">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="fda78-603">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-604">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-604">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-605">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="fda78-605">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="fda78-606">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="fda78-606">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-607">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-607">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-608">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="fda78-608">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-609">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-609">Az.IotHub</span></span>
* <span data-ttu-id="fda78-610">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fda78-610">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="fda78-611">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-611">New Cmdlets are:</span></span>
    - <span data-ttu-id="fda78-612">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="fda78-612">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="fda78-613">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="fda78-613">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-614">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-615">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="fda78-615">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-616">Az.Monitor</span></span>
* <span data-ttu-id="fda78-617">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="fda78-617">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-618">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-618">Az.Network</span></span>
* <span data-ttu-id="fda78-619">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="fda78-619">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="fda78-620">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-620">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="fda78-621">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="fda78-621">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="fda78-622">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="fda78-622">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="fda78-623">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="fda78-623">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="fda78-624">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="fda78-624">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-625">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-625">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-626">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="fda78-626">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-627">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-627">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-628">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="fda78-628">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="fda78-629">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="fda78-629">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="fda78-630">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="fda78-630">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="fda78-631">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="fda78-631">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="fda78-632">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="fda78-632">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="fda78-633">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="fda78-633">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-634">Az.Resources</span></span>
* <span data-ttu-id="fda78-635">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="fda78-635">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="fda78-636">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="fda78-636">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="fda78-637">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="fda78-637">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="fda78-638">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="fda78-638">Added example.</span></span>
* <span data-ttu-id="fda78-639">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="fda78-639">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="fda78-640">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="fda78-640">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-641">Az.Sql</span></span>
* <span data-ttu-id="fda78-642">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="fda78-642">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="fda78-643">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-643">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="fda78-644">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fda78-644">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="fda78-645">Az.Support</span><span class="sxs-lookup"><span data-stu-id="fda78-645">Az.Support</span></span>
* <span data-ttu-id="fda78-646">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="fda78-646">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-647">Az.Websites</span></span>
* <span data-ttu-id="fda78-648">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="fda78-648">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="fda78-649">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="fda78-649">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="fda78-650">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="fda78-650">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="fda78-651">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="fda78-651">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="fda78-652">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="fda78-652">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="fda78-653">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-653">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-654">Az.Accounts</span></span>
* <span data-ttu-id="fda78-655">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="fda78-655">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="fda78-656">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="fda78-656">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="fda78-657">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="fda78-657">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-658">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-658">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-659">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="fda78-659">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="fda78-660">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="fda78-660">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="fda78-661">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="fda78-661">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="fda78-662">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="fda78-662">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-663">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-663">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-664">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="fda78-664">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-665">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-665">Az.IotHub</span></span>
* <span data-ttu-id="fda78-666">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-666">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="fda78-667">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-667">New Cmdlets are:</span></span>
    - <span data-ttu-id="fda78-668">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-668">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-669">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-669">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-670">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-670">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-671">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-671">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="fda78-672">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-672">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="fda78-673">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-673">New Cmdlets are:</span></span>
    - <span data-ttu-id="fda78-674">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="fda78-674">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="fda78-675">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="fda78-675">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="fda78-676">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="fda78-676">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="fda78-677">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="fda78-677">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="fda78-678">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-678">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="fda78-679">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-679">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="fda78-680">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-680">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="fda78-681">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-681">New Cmdlets are:</span></span>
    - <span data-ttu-id="fda78-682">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="fda78-682">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="fda78-683">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="fda78-683">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="fda78-684">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fda78-684">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-685">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-685">Az.Monitor</span></span>
* <span data-ttu-id="fda78-686">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="fda78-686">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-687">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-687">Az.Network</span></span>
* <span data-ttu-id="fda78-688">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="fda78-688">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="fda78-689">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="fda78-689">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="fda78-690">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="fda78-690">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="fda78-691">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="fda78-691">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-692">Az.Resources</span></span>
* <span data-ttu-id="fda78-693">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="fda78-693">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="fda78-694">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="fda78-694">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="fda78-695">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="fda78-695">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="fda78-696">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="fda78-696">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="fda78-697">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="fda78-697">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="fda78-698">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="fda78-698">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="fda78-699">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="fda78-699">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="fda78-700">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-700">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="fda78-701">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-701">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="fda78-702">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-702">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="fda78-703">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-703">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="fda78-704">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-704">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="fda78-705">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-705">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="fda78-706">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="fda78-706">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-707">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-707">Az.Sql</span></span>
* <span data-ttu-id="fda78-708">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="fda78-708">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="fda78-709">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="fda78-709">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="fda78-710">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="fda78-710">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="fda78-711">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="fda78-711">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="fda78-712">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="fda78-712">Remove an LTR backup</span></span>
    - <span data-ttu-id="fda78-713">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="fda78-713">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="fda78-714">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="fda78-714">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="fda78-715">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-715">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="fda78-716">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-716">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-717">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-717">Az.Storage</span></span>
* <span data-ttu-id="fda78-718">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-718">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="fda78-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="fda78-719">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="fda78-720">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="fda78-720">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="fda78-721">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-721">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="fda78-722">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="fda78-722">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-723">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-723">Az.Websites</span></span>
* <span data-ttu-id="fda78-724">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="fda78-724">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="fda78-725">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="fda78-725">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="fda78-726">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fda78-726">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="fda78-727">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="fda78-727">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="fda78-728">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="fda78-728">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="fda78-729">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-729">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-730">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-730">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-731">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="fda78-731">Updated client side telemetry.</span></span>
* <span data-ttu-id="fda78-732">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fda78-732">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="fda78-733">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="fda78-733">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-734">Az.Accounts</span></span>
* <span data-ttu-id="fda78-735">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="fda78-735">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-736">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-736">Az.Automation</span></span>
* <span data-ttu-id="fda78-737">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="fda78-737">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-738">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-738">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-739">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="fda78-739">Updated SDK to 7.0</span></span>
* <span data-ttu-id="fda78-740">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="fda78-740">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-741">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-741">Az.Compute</span></span>
* <span data-ttu-id="fda78-742">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="fda78-742">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-743">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-744">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="fda78-744">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-745">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-745">Az.IotHub</span></span>
* <span data-ttu-id="fda78-746">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-746">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="fda78-747">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-747">New Cmdlets are:</span></span>
    - <span data-ttu-id="fda78-748">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-748">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-749">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-749">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-750">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-750">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="fda78-751">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="fda78-751">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-752">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-752">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-753">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="fda78-753">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-754">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-754">Az.Monitor</span></span>
* <span data-ttu-id="fda78-755">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="fda78-755">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="fda78-756">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="fda78-756">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="fda78-757">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="fda78-757">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-758">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-758">Az.Network</span></span>
* <span data-ttu-id="fda78-759">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="fda78-759">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="fda78-760">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="fda78-760">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="fda78-761">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="fda78-761">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="fda78-762">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="fda78-762">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="fda78-763">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="fda78-763">No new cmdlets are added.</span></span> <span data-ttu-id="fda78-764">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="fda78-764">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-765">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-765">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-766">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="fda78-766">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-767">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-767">Az.Resources</span></span>
* <span data-ttu-id="fda78-768">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="fda78-768">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="fda78-769">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fda78-769">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="fda78-770">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="fda78-770">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="fda78-771">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="fda78-771">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="fda78-772">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="fda78-772">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="fda78-773">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="fda78-773">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="fda78-774">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="fda78-774">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="fda78-775">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-775">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-776">Az.Sql</span></span>
* <span data-ttu-id="fda78-777">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="fda78-777">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="fda78-778">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="fda78-778">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="fda78-779">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="fda78-779">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="fda78-780">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fda78-780">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="fda78-781">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="fda78-781">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fda78-782">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fda78-782">Az.StorageSync</span></span>
* <span data-ttu-id="fda78-783">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="fda78-783">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="fda78-784">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-784">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-785">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-785">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-786">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fda78-786">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="fda78-787">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-787">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-788">Az.Accounts</span></span>
* <span data-ttu-id="fda78-789">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="fda78-789">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="fda78-790">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="fda78-790">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-791">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-791">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-792">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="fda78-792">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="fda78-793">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="fda78-793">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="fda78-794">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="fda78-794">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="fda78-795">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="fda78-795">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-796">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-796">Az.Compute</span></span>
* <span data-ttu-id="fda78-797">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="fda78-797">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="fda78-798">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="fda78-798">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="fda78-799">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fda78-799">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="fda78-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-800">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="fda78-801">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="fda78-801">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-802">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-802">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-803">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="fda78-803">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="fda78-804">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="fda78-804">Az.DeploymentManager</span></span>
* <span data-ttu-id="fda78-805">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="fda78-805">Adds LIST operations for resources</span></span>
* <span data-ttu-id="fda78-806">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="fda78-806">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-807">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-807">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-808">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="fda78-808">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-809">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-809">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-810">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="fda78-810">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-811">Az.Network</span></span>
* <span data-ttu-id="fda78-812">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="fda78-812">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="fda78-813">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fda78-813">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="fda78-814">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="fda78-814">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="fda78-815">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="fda78-815">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="fda78-816">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="fda78-816">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="fda78-817">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="fda78-817">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="fda78-818">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="fda78-818">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="fda78-819">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fda78-819">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="fda78-820">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-820">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-821">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="fda78-822">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-822">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="fda78-823">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fda78-823">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="fda78-824">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="fda78-824">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-825">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-825">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-826">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="fda78-826">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="fda78-827">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="fda78-827">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="fda78-828">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="fda78-828">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="fda78-829">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="fda78-829">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-830">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-830">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-831">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="fda78-831">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="fda78-832">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="fda78-832">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-833">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-833">Az.Resources</span></span>
* <span data-ttu-id="fda78-834">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="fda78-834">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="fda78-835">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="fda78-835">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-836">Az.Sql</span></span>
<span data-ttu-id="fda78-837">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="fda78-837">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-838">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-838">Az.Storage</span></span>
* <span data-ttu-id="fda78-839">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-839">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="fda78-840">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-840">New-AzStorageAccount</span></span>
* <span data-ttu-id="fda78-841">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="fda78-841">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="fda78-842">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-842">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-843">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-843">Az.Websites</span></span>
* <span data-ttu-id="fda78-844">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="fda78-844">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="fda78-845">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="fda78-845">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="fda78-846">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="fda78-846">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-847">Az.Accounts</span></span>
* <span data-ttu-id="fda78-848">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="fda78-848">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-849">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-849">Az.Cdn</span></span>
* <span data-ttu-id="fda78-850">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-850">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-851">Az.Compute</span></span>
* <span data-ttu-id="fda78-852">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="fda78-852">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="fda78-853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-853">Az.ContainerInstance</span></span>
* <span data-ttu-id="fda78-854">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-854">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="fda78-855">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="fda78-855">Az.DataBoxEdge</span></span>
* <span data-ttu-id="fda78-856">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="fda78-856">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fda78-857">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-857">Get the Edge Storage Container</span></span>
* <span data-ttu-id="fda78-858">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="fda78-858">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fda78-859">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-859">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="fda78-860">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="fda78-860">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fda78-861">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-861">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="fda78-862">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="fda78-862">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="fda78-863">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-863">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="fda78-864">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-864">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fda78-865">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-865">Get the Edge Storage Account</span></span>
* <span data-ttu-id="fda78-866">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-866">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fda78-867">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-867">Create new Edge Storage Account</span></span>
* <span data-ttu-id="fda78-868">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="fda78-868">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="fda78-869">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="fda78-869">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="fda78-870">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="fda78-870">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="fda78-871">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="fda78-871">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="fda78-872">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="fda78-872">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="fda78-873">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="fda78-873">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-874">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-874">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-875">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fda78-875">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="fda78-876">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="fda78-876">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="fda78-877">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="fda78-877">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="fda78-878">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fda78-878">Az.DevTestLabs</span></span>
* <span data-ttu-id="fda78-879">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="fda78-879">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-880">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-880">Az.EventHub</span></span>
* <span data-ttu-id="fda78-881">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="fda78-881">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-882">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-882">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-883">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="fda78-883">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="fda78-884">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fda78-884">Az.MachineLearning</span></span>
* <span data-ttu-id="fda78-885">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="fda78-885">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="fda78-886">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fda78-886">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="fda78-887">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="fda78-887">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="fda78-888">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fda78-888">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="fda78-889">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fda78-889">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="fda78-890">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fda78-890">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="fda78-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="fda78-891">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="fda78-892">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="fda78-892">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-893">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-893">Az.Network</span></span>
* <span data-ttu-id="fda78-894">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="fda78-894">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-895">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-896">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-896">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="fda78-897">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-897">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="fda78-898">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-898">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="fda78-899">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-899">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-900">Az.Resources</span></span>
* <span data-ttu-id="fda78-901">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="fda78-901">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-902">Az.Sql</span></span>
* <span data-ttu-id="fda78-903">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="fda78-903">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="fda78-904">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="fda78-904">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="fda78-905">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fda78-905">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="fda78-906">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="fda78-906">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-907">Az.Storage</span></span>
* <span data-ttu-id="fda78-908">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="fda78-908">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="fda78-909">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-909">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="fda78-910">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="fda78-910">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="fda78-911">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-911">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="fda78-912">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-912">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="fda78-913">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-913">General</span></span>
* <span data-ttu-id="fda78-914">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="fda78-914">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-915">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-915">Az.Accounts</span></span>
* <span data-ttu-id="fda78-916">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="fda78-916">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="fda78-917">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="fda78-917">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-918">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-918">Az.Batch</span></span>
* <span data-ttu-id="fda78-919">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="fda78-919">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-920">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-920">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-921">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="fda78-921">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-922">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-922">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-923">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="fda78-923">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="fda78-924">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="fda78-924">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fda78-925">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fda78-925">Az.HealthcareApis</span></span>
* <span data-ttu-id="fda78-926">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="fda78-926">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-927">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-927">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-928">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="fda78-928">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="fda78-929">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="fda78-929">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="fda78-930">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="fda78-930">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-931">Az.Monitor</span></span>
* <span data-ttu-id="fda78-932">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="fda78-932">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="fda78-933">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="fda78-933">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="fda78-934">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="fda78-934">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-935">Az.Network</span></span>
* <span data-ttu-id="fda78-936">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="fda78-936">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-937">Az.Resources</span></span>
* <span data-ttu-id="fda78-938">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="fda78-938">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="fda78-939">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="fda78-939">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-940">Az.Sql</span></span>
* <span data-ttu-id="fda78-941">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="fda78-941">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-942">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-942">Az.Storage</span></span>
* <span data-ttu-id="fda78-943">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="fda78-943">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="fda78-944">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fda78-944">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="fda78-945">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fda78-945">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="fda78-946">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="fda78-946">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="fda78-947">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="fda78-947">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="fda78-948">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="fda78-948">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="fda78-949">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="fda78-949">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="fda78-950">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-950">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="fda78-951">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-951">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="fda78-952">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="fda78-952">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="fda78-953">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fda78-953">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="fda78-954">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="fda78-954">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="fda78-955">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fda78-955">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="fda78-956">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-956">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-957">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-957">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-958">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="fda78-958">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="fda78-959">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="fda78-959">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-960">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-960">Az.Compute</span></span>
* <span data-ttu-id="fda78-961">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="fda78-961">VM Reapply feature</span></span>
    - <span data-ttu-id="fda78-962">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="fda78-962">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="fda78-963">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="fda78-963">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="fda78-964">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-964">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="fda78-965">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="fda78-965">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="fda78-966">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-966">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="fda78-967">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="fda78-967">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="fda78-968">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="fda78-968">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="fda78-969">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="fda78-969">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="fda78-970">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fda78-970">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="fda78-971">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-971">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="fda78-972">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="fda78-972">Az.DataBoxEdge</span></span>
* <span data-ttu-id="fda78-973">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-973">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fda78-974">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="fda78-974">Get the Order</span></span>
* <span data-ttu-id="fda78-975">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-975">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fda78-976">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="fda78-976">Create new Order</span></span>
* <span data-ttu-id="fda78-977">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-977">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="fda78-978">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="fda78-978">Remove the Order</span></span>
* <span data-ttu-id="fda78-979">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="fda78-979">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="fda78-980">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="fda78-980">Now creates Local Share</span></span>
* <span data-ttu-id="fda78-981">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-981">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="fda78-982">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="fda78-982">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="fda78-983">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-983">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="fda78-984">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="fda78-984">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="fda78-985">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-985">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fda78-986">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="fda78-986">Gets the information about Triggers</span></span>
* <span data-ttu-id="fda78-987">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-987">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fda78-988">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="fda78-988">Create new Triggers</span></span>
* <span data-ttu-id="fda78-989">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-989">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="fda78-990">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="fda78-990">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-991">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-991">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-992">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="fda78-992">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="fda78-993">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="fda78-993">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-994">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-994">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-995">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="fda78-995">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-996">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-996">Az.EventHub</span></span>
* <span data-ttu-id="fda78-997">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="fda78-997">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-998">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-998">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-999">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="fda78-999">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="fda78-1000">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1000">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="fda78-1001">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="fda78-1001">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="fda78-1002">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1002">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1003">Az.Network</span></span>
* <span data-ttu-id="fda78-1004">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1004">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="fda78-1005">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="fda78-1005">Az.PrivateDns</span></span>
* <span data-ttu-id="fda78-1006">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1006">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1007">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1007">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1008">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="fda78-1008">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="fda78-1009">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fda78-1009">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="fda78-1010">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1010">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fda78-1011">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fda78-1011">Az.RedisCache</span></span>
* <span data-ttu-id="fda78-1012">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1012">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="fda78-1013">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1013">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="fda78-1014">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="fda78-1014">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1015">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1015">Az.Resources</span></span>
- <span data-ttu-id="fda78-1016">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="fda78-1016">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="fda78-1017">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="fda78-1017">Updated create policy definition help example</span></span>
- <span data-ttu-id="fda78-1018">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="fda78-1018">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="fda78-1019">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="fda78-1019">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="fda78-1020">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="fda78-1020">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1021">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1021">Az.Sql</span></span>
* <span data-ttu-id="fda78-1022">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="fda78-1022">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="fda78-1023">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="fda78-1023">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="fda78-1024">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1024">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="fda78-1025">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-1025">General</span></span>
* <span data-ttu-id="fda78-1026">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="fda78-1026">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-1027">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1027">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1028">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1028">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="fda78-1029">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fda78-1029">Az.Advisor</span></span>
* <span data-ttu-id="fda78-1030">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda78-1030">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-1031">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-1031">Az.Batch</span></span>
* <span data-ttu-id="fda78-1032">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1032">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="fda78-1033">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1033">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="fda78-1034">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1034">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="fda78-1035">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1035">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="fda78-1036">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1036">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="fda78-1037">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1037">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="fda78-1038">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="fda78-1038">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="fda78-1039">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="fda78-1039">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="fda78-1040">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="fda78-1040">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="fda78-1041">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1041">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="fda78-1042">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1042">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="fda78-1043">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1043">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="fda78-1044">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1044">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="fda78-1045">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1045">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="fda78-1046">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1046">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="fda78-1047">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1047">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="fda78-1048">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1048">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="fda78-1049">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1049">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="fda78-1050">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1050">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="fda78-1051">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="fda78-1051">This operation is no longer supported.</span></span>
* <span data-ttu-id="fda78-1052">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1052">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="fda78-1053">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1053">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="fda78-1054">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1054">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="fda78-1055">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1055">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="fda78-1056">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="fda78-1056">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="fda78-1057">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="fda78-1057">New non-verified images are also now returned.</span></span> <span data-ttu-id="fda78-1058">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="fda78-1058">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="fda78-1059">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1059">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="fda78-1060">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="fda78-1060">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="fda78-1061">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1061">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="fda78-1062">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="fda78-1062">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="fda78-1063">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1063">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="fda78-1064">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="fda78-1064">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="fda78-1065">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fda78-1065">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="fda78-1066">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="fda78-1066">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="fda78-1067">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="fda78-1067">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-1068">Az.Cdn</span></span>
* <span data-ttu-id="fda78-1069">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="fda78-1069">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="fda78-1070">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="fda78-1070">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1071">Az.Compute</span></span>
* <span data-ttu-id="fda78-1072">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="fda78-1072">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="fda78-1073">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="fda78-1073">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="fda78-1074">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fda78-1074">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="fda78-1075">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1075">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fda78-1076">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1076">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="fda78-1077">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="fda78-1077">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="fda78-1078">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-1078">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="fda78-1079">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="fda78-1079">Breaking changes</span></span>
    - <span data-ttu-id="fda78-1080">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="fda78-1080">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="fda78-1081">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="fda78-1081">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1082">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1082">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1083">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1083">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-1084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-1084">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-1085">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="fda78-1085">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="fda78-1086">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="fda78-1086">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="fda78-1087">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="fda78-1087">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="fda78-1088">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="fda78-1088">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="fda78-1089">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="fda78-1089">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="fda78-1090">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="fda78-1090">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-1091">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-1091">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-1092">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="fda78-1092">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-1093">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-1094">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="fda78-1094">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="fda78-1095">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="fda78-1095">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="fda78-1096">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1096">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="fda78-1097">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="fda78-1097">Removed five cmdlets:</span></span>
    - <span data-ttu-id="fda78-1098">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fda78-1098">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fda78-1099">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fda78-1099">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fda78-1100">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="fda78-1100">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="fda78-1101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fda78-1101">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="fda78-1102">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fda78-1102">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="fda78-1103">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1103">Added three cmdlets:</span></span>
    - <span data-ttu-id="fda78-1104">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="fda78-1104">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="fda78-1105">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="fda78-1105">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="fda78-1106">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="fda78-1106">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="fda78-1107">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="fda78-1107">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="fda78-1108">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="fda78-1108">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="fda78-1109">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="fda78-1109">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="fda78-1110">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="fda78-1110">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="fda78-1111">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="fda78-1111">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="fda78-1112">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="fda78-1112">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="fda78-1113">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="fda78-1113">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="fda78-1114">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="fda78-1114">Added some scenario test cases.</span></span>
* <span data-ttu-id="fda78-1115">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1115">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-1116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1116">Az.IotHub</span></span>
* <span data-ttu-id="fda78-1117">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="fda78-1117">Breaking changes:</span></span>
    - <span data-ttu-id="fda78-1118">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="fda78-1118">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fda78-1119">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1119">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fda78-1120">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="fda78-1120">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fda78-1121">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1121">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fda78-1122">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="fda78-1122">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="fda78-1123">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="fda78-1123">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="fda78-1124">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1124">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="fda78-1125">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1125">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="fda78-1126">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="fda78-1126">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fda78-1127">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1127">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="fda78-1128">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="fda78-1128">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="fda78-1129">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1129">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1130">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1130">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1131">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1131">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1132">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1132">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="fda78-1133">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1133">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="fda78-1134">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1134">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1135">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1135">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1136">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1136">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1137">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1137">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1138">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1138">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1139">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="fda78-1139">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1140">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1140">Az.Resources</span></span>
* <span data-ttu-id="fda78-1141">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="fda78-1141">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1142">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1142">Az.Network</span></span>
* <span data-ttu-id="fda78-1143">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="fda78-1143">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="fda78-1144">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1144">Updated cmdlet:</span></span>
        - <span data-ttu-id="fda78-1145">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1145">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1146">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1146">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1147">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1147">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1148">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1148">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1149">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="fda78-1150">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="fda78-1150">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="fda78-1151">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1151">New cmdlet:</span></span>
        - <span data-ttu-id="fda78-1152">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="fda78-1152">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="fda78-1153">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="fda78-1153">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="fda78-1154">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1154">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="fda78-1155">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1155">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="fda78-1156">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="fda78-1156">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="fda78-1157">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="fda78-1157">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="fda78-1158">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1158">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="fda78-1159">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1159">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="fda78-1160">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1160">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-1161">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="fda78-1161">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="fda78-1162">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-1162">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fda78-1163">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-1163">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fda78-1164">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-1164">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="fda78-1165">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1165">Set-AzVirtualHub</span></span>
* <span data-ttu-id="fda78-1166">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="fda78-1166">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="fda78-1167">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="fda78-1167">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fda78-1168">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1168">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="fda78-1169">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1169">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="fda78-1170">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1170">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="fda78-1171">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1171">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="fda78-1172">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1172">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="fda78-1173">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1173">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-1174">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1174">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="fda78-1175">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="fda78-1175">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fda78-1176">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1176">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fda78-1177">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1177">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fda78-1178">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1178">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fda78-1179">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1179">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="fda78-1180">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-1180">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="fda78-1181">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="fda78-1181">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="fda78-1182">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1182">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-1183">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="fda78-1183">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="fda78-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="fda78-1184">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="fda78-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="fda78-1185">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="fda78-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="fda78-1186">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="fda78-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1187">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="fda78-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-1188">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="fda78-1189">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="fda78-1189">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fda78-1190">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-1190">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="fda78-1191">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1191">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="fda78-1192">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="fda78-1192">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="fda78-1193">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="fda78-1193">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="fda78-1194">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="fda78-1194">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="fda78-1195">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-1195">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="fda78-1196">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-1196">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="fda78-1197">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="fda78-1197">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="fda78-1198">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1198">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="fda78-1199">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1199">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="fda78-1200">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1200">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-1201">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1201">New-AzIpGroup</span></span>
        - <span data-ttu-id="fda78-1202">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1202">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="fda78-1203">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1203">Get-AzIpGroup</span></span>
        - <span data-ttu-id="fda78-1204">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1204">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-1206">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="fda78-1206">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1207">Az.Sql</span></span>
* <span data-ttu-id="fda78-1208">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="fda78-1208">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="fda78-1209">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="fda78-1209">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="fda78-1210">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="fda78-1210">Removed deprecated aliases:</span></span>
* <span data-ttu-id="fda78-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="fda78-1211">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="fda78-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="fda78-1212">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="fda78-1213">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-1213">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="fda78-1214">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="fda78-1214">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="fda78-1215">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="fda78-1215">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="fda78-1216">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fda78-1216">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1217">Az.Storage</span></span>
* <span data-ttu-id="fda78-1218">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-1218">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="fda78-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1219">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="fda78-1220">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1220">Set-AzStorageAccount</span></span>
* <span data-ttu-id="fda78-1221">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="fda78-1221">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="fda78-1222">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fda78-1222">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="fda78-1223">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fda78-1223">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="fda78-1224">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1224">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="fda78-1225">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-1225">General</span></span>
* <span data-ttu-id="fda78-1226">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1226">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-1227">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1227">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1228">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="fda78-1228">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-1229">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1229">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-1230">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fda78-1230">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="fda78-1231">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="fda78-1231">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-1232">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1232">Az.Automation</span></span>
* <span data-ttu-id="fda78-1233">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="fda78-1233">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-1234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-1234">Az.Batch</span></span>
* <span data-ttu-id="fda78-1235">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="fda78-1235">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1236">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1236">Az.Compute</span></span>
* <span data-ttu-id="fda78-1237">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-1237">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="fda78-1238">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1238">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="fda78-1239">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="fda78-1239">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="fda78-1240">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="fda78-1240">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1241">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1241">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1242">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="fda78-1242">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="fda78-1243">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="fda78-1243">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="fda78-1244">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1244">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-1246">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="fda78-1246">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="fda78-1247">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="fda78-1247">Az.HealthcareApis</span></span>
* <span data-ttu-id="fda78-1248">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1248">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="fda78-1249">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="fda78-1249">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="fda78-1250">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="fda78-1250">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="fda78-1251">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="fda78-1251">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-1252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1252">Az.IotHub</span></span>
* <span data-ttu-id="fda78-1253">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="fda78-1253">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="fda78-1254">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="fda78-1254">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-1255">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-1255">Az.Monitor</span></span>
* <span data-ttu-id="fda78-1256">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="fda78-1256">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="fda78-1257">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="fda78-1257">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="fda78-1258">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="fda78-1258">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="fda78-1259">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fda78-1259">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1260">Az.Network</span></span>
* <span data-ttu-id="fda78-1261">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="fda78-1261">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="fda78-1262">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="fda78-1262">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="fda78-1263">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1263">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-1264">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-1264">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="fda78-1265">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1265">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fda78-1266">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="fda78-1266">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="fda78-1267">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1267">Updated cmdlets:</span></span>
        - <span data-ttu-id="fda78-1268">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1268">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fda78-1269">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1269">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fda78-1270">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1270">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fda78-1271">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="fda78-1271">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="fda78-1272">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="fda78-1272">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="fda78-1273">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="fda78-1273">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="fda78-1274">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="fda78-1274">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fda78-1275">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fda78-1275">Az.RedisCache</span></span>
* <span data-ttu-id="fda78-1276">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="fda78-1276">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1277">Az.Sql</span></span>
* <span data-ttu-id="fda78-1278">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="fda78-1278">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1279">Az.Storage</span></span>
* <span data-ttu-id="fda78-1280">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="fda78-1280">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="fda78-1281">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="fda78-1281">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fda78-1282">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fda78-1282">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="fda78-1283">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="fda78-1283">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="fda78-1284">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1284">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fda78-1285">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fda78-1285">Az.StorageSync</span></span>
* <span data-ttu-id="fda78-1286">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="fda78-1286">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1287">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1287">Az.Websites</span></span>
* <span data-ttu-id="fda78-1288">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="fda78-1288">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="fda78-1289">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1289">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fda78-1290">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1290">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-1291">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="fda78-1291">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="fda78-1292">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="fda78-1292">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="fda78-1293">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1293">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-1294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1294">Az.Automation</span></span>
* <span data-ttu-id="fda78-1295">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="fda78-1295">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="fda78-1296">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="fda78-1296">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="fda78-1297">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="fda78-1297">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1298">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1298">Az.Compute</span></span>
* <span data-ttu-id="fda78-1299">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1299">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="fda78-1300">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1300">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fda78-1301">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="fda78-1301">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="fda78-1302">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="fda78-1302">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="fda78-1303">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="fda78-1303">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="fda78-1304">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fda78-1304">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="fda78-1305">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="fda78-1305">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="fda78-1306">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="fda78-1306">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="fda78-1307">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="fda78-1307">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1308">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1309">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="fda78-1309">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="fda78-1310">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="fda78-1310">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-1311">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-1311">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-1312">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="fda78-1312">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-1313">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1313">Az.IotHub</span></span>
* <span data-ttu-id="fda78-1314">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="fda78-1314">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="fda78-1315">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="fda78-1315">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="fda78-1316">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="fda78-1316">New cmdlets are:</span></span>
    - <span data-ttu-id="fda78-1317">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fda78-1317">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fda78-1318">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fda78-1318">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fda78-1319">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fda78-1319">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="fda78-1320">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="fda78-1320">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-1321">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-1321">Az.Monitor</span></span>
* <span data-ttu-id="fda78-1322">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="fda78-1322">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="fda78-1323">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="fda78-1323">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="fda78-1324">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="fda78-1324">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="fda78-1325">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1325">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="fda78-1326">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="fda78-1326">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="fda78-1327">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="fda78-1327">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="fda78-1328">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fda78-1328">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="fda78-1329">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="fda78-1329">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="fda78-1330">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="fda78-1330">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fda78-1331">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="fda78-1331">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="fda78-1332">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="fda78-1332">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="fda78-1333">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="fda78-1333">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="fda78-1334">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="fda78-1334">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="fda78-1335">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="fda78-1335">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="fda78-1336">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="fda78-1336">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="fda78-1337">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="fda78-1337">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="fda78-1338">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="fda78-1338">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="fda78-1339">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-1339">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="fda78-1340">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="fda78-1340">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="fda78-1341">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-1341">Overall improved help files</span></span>
* <span data-ttu-id="fda78-1342">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="fda78-1342">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1343">Az.Network</span></span>
* <span data-ttu-id="fda78-1344">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="fda78-1344">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="fda78-1345">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="fda78-1345">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="fda78-1346">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="fda78-1346">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="fda78-1347">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="fda78-1347">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="fda78-1348">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="fda78-1348">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="fda78-1349">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="fda78-1349">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="fda78-1350">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="fda78-1350">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="fda78-1351">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fda78-1351">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="fda78-1352">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-1352">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="fda78-1353">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="fda78-1353">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="fda78-1354">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1354">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="fda78-1355">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="fda78-1355">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="fda78-1356">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1356">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1357">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="fda78-1357">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="fda78-1358">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1358">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="fda78-1359">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1359">Updated cmdlet:</span></span>
        - <span data-ttu-id="fda78-1360">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fda78-1360">New-VpnSite</span></span>
        - <span data-ttu-id="fda78-1361">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="fda78-1361">Update-VpnSite</span></span>
        - <span data-ttu-id="fda78-1362">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1362">New-VpnConnection</span></span>
        - <span data-ttu-id="fda78-1363">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1363">Update-VpnConnection</span></span>
* <span data-ttu-id="fda78-1364">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="fda78-1364">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1365">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1365">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1366">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="fda78-1366">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="fda78-1367">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="fda78-1367">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1368">Az.Resources</span></span>
* <span data-ttu-id="fda78-1369">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="fda78-1369">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-1370">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1370">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-1371">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="fda78-1371">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="fda78-1372">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="fda78-1372">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="fda78-1373">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fda78-1373">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fda78-1374">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fda78-1374">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fda78-1375">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fda78-1375">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fda78-1376">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fda78-1376">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="fda78-1377">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fda78-1377">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fda78-1378">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fda78-1378">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fda78-1379">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fda78-1379">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fda78-1380">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fda78-1380">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fda78-1381">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="fda78-1381">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="fda78-1382">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="fda78-1382">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="fda78-1383">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="fda78-1383">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="fda78-1384">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="fda78-1384">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="fda78-1385">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="fda78-1385">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="fda78-1386">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="fda78-1386">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fda78-1387">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fda78-1387">Az.SignalR</span></span>
* <span data-ttu-id="fda78-1388">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="fda78-1388">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1389">Az.Sql</span></span>
* <span data-ttu-id="fda78-1390">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="fda78-1390">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="fda78-1391">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="fda78-1391">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="fda78-1392">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-1392">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fda78-1393">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="fda78-1393">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="fda78-1394">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="fda78-1394">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1395">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1395">Az.Storage</span></span>
* <span data-ttu-id="fda78-1396">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="fda78-1396">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="fda78-1397">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="fda78-1397">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="fda78-1398">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fda78-1398">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="fda78-1399">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fda78-1399">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="fda78-1400">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="fda78-1400">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="fda78-1401">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fda78-1401">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="fda78-1402">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fda78-1402">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="fda78-1403">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-1403">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fda78-1404">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-1404">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fda78-1405">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-1405">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="fda78-1406">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fda78-1406">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1407">Az.Websites</span></span>
* <span data-ttu-id="fda78-1408">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="fda78-1408">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="fda78-1409">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="fda78-1409">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="fda78-1410">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="fda78-1410">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="fda78-1411">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1411">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="fda78-1412">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-1412">General</span></span>
* <span data-ttu-id="fda78-1413">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="fda78-1413">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-1414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1414">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1415">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="fda78-1415">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="fda78-1416">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fda78-1416">Az.Aks</span></span>
* <span data-ttu-id="fda78-1417">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="fda78-1417">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="fda78-1418">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="fda78-1418">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-1419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1419">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-1420">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="fda78-1420">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="fda78-1421">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="fda78-1421">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="fda78-1422">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="fda78-1422">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="fda78-1423">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="fda78-1423">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="fda78-1424">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="fda78-1424">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-1425">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-1425">Az.Batch</span></span>
* <span data-ttu-id="fda78-1426">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="fda78-1426">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-1427">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-1427">Az.Cdn</span></span>
* <span data-ttu-id="fda78-1428">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="fda78-1428">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1429">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1429">Az.Compute</span></span>
* <span data-ttu-id="fda78-1430">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1430">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="fda78-1431">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-1431">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="fda78-1432">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="fda78-1432">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="fda78-1433">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1433">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="fda78-1434">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="fda78-1434">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="fda78-1435">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="fda78-1435">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="fda78-1436">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="fda78-1436">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="fda78-1437">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="fda78-1437">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1438">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1439">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="fda78-1439">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="fda78-1440">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="fda78-1440">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="fda78-1441">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="fda78-1441">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="fda78-1442">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="fda78-1442">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-1444">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="fda78-1444">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-1445">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1445">Az.EventHub</span></span>
* <span data-ttu-id="fda78-1446">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-1446">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="fda78-1447">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="fda78-1447">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="fda78-1448">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fda78-1448">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="fda78-1449">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="fda78-1449">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="fda78-1450">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fda78-1450">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fda78-1451">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="fda78-1451">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-1452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-1452">Az.Monitor</span></span>
* <span data-ttu-id="fda78-1453">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-1453">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1454">Az.Network</span></span>
* <span data-ttu-id="fda78-1455">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1455">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="fda78-1456">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="fda78-1456">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="fda78-1457">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="fda78-1457">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="fda78-1458">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="fda78-1458">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="fda78-1459">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="fda78-1459">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="fda78-1460">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fda78-1460">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="fda78-1461">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="fda78-1461">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-1462">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1462">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-1463">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="fda78-1463">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="fda78-1464">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="fda78-1464">Added example</span></span>
    - <span data-ttu-id="fda78-1465">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="fda78-1465">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="fda78-1466">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="fda78-1466">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="fda78-1467">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="fda78-1467">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1468">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1469">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1469">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1470">Az.Resources</span></span>
* <span data-ttu-id="fda78-1471">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="fda78-1471">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="fda78-1472">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="fda78-1472">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="fda78-1473">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="fda78-1473">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="fda78-1474">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-1474">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-1475">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-1475">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-1476">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-1476">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="fda78-1477">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="fda78-1477">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="fda78-1478">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="fda78-1478">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-1479">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1479">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-1480">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="fda78-1480">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="fda78-1481">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="fda78-1481">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="fda78-1482">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="fda78-1482">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="fda78-1483">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="fda78-1483">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="fda78-1484">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="fda78-1484">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="fda78-1485">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fda78-1485">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1486">Az.Sql</span></span>
* <span data-ttu-id="fda78-1487">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="fda78-1487">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1488">Az.Storage</span></span>
* <span data-ttu-id="fda78-1489">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="fda78-1489">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="fda78-1490">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="fda78-1490">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="fda78-1491">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fda78-1491">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="fda78-1492">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-1492">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="fda78-1493">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="fda78-1493">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="fda78-1494">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-1494">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1495">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1495">Az.Websites</span></span>
* <span data-ttu-id="fda78-1496">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fda78-1496">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="fda78-1497">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1497">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-1498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1498">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1499">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fda78-1499">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="fda78-1500">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1500">Az.ApplicationInsights</span></span>
* <span data-ttu-id="fda78-1501">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="fda78-1501">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-1502">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1502">Az.Automation</span></span>
* <span data-ttu-id="fda78-1503">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="fda78-1503">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-1504">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1504">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-1505">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="fda78-1505">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1506">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1506">Az.Compute</span></span>
* <span data-ttu-id="fda78-1507">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="fda78-1507">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fda78-1508">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fda78-1508">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fda78-1509">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="fda78-1509">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="fda78-1510">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="fda78-1510">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1511">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1511">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1512">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-1512">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="fda78-1513">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="fda78-1513">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-1514">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1514">Az.EventHub</span></span>
* <span data-ttu-id="fda78-1515">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fda78-1515">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fda78-1516">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="fda78-1516">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-1517">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-1517">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-1518">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="fda78-1518">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fda78-1519">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fda78-1519">Az.LogicApp</span></span>
* <span data-ttu-id="fda78-1520">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="fda78-1520">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="fda78-1521">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="fda78-1521">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="fda78-1522">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1522">Az.ManagedServices</span></span>
* <span data-ttu-id="fda78-1523">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="fda78-1523">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1524">Az.Network</span></span>
* <span data-ttu-id="fda78-1525">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="fda78-1525">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="fda78-1526">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1526">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1527">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-1527">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fda78-1528">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1528">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fda78-1529">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1529">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1530">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1530">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1531">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1531">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1532">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1532">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="fda78-1533">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="fda78-1533">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="fda78-1534">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1534">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="fda78-1535">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="fda78-1535">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="fda78-1536">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="fda78-1536">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="fda78-1537">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fda78-1537">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="fda78-1538">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="fda78-1538">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="fda78-1539">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="fda78-1539">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="fda78-1540">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="fda78-1540">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="fda78-1541">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="fda78-1541">Updated cmdlets</span></span>
        - <span data-ttu-id="fda78-1542">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1542">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fda78-1543">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1543">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="fda78-1544">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1544">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="fda78-1545">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1545">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fda78-1546">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-1546">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="fda78-1547">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1547">Updated cmdlet:</span></span>
        - <span data-ttu-id="fda78-1548">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1548">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fda78-1549">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1549">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="fda78-1550">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1550">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="fda78-1551">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="fda78-1551">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="fda78-1552">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="fda78-1552">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="fda78-1553">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="fda78-1553">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-1554">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1554">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-1555">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="fda78-1555">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="fda78-1556">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="fda78-1556">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1557">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1558">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1558">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fda78-1559">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1559">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="fda78-1560">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1560">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="fda78-1561">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1561">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="fda78-1562">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1562">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="fda78-1563">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1563">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fda78-1564">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1564">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="fda78-1565">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1565">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="fda78-1566">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1566">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="fda78-1567">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="fda78-1567">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1568">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1568">Az.Resources</span></span>
- <span data-ttu-id="fda78-1569">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-1569">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="fda78-1570">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="fda78-1570">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-1571">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-1571">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-1572">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="fda78-1572">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="fda78-1573">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="fda78-1573">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1574">Az.Sql</span></span>
* <span data-ttu-id="fda78-1575">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fda78-1575">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="fda78-1576">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="fda78-1576">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="fda78-1577">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="fda78-1577">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1578">Az.Storage</span></span>
* <span data-ttu-id="fda78-1579">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="fda78-1579">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fda78-1580">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fda78-1580">Az.StorageSync</span></span>
* <span data-ttu-id="fda78-1581">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="fda78-1581">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="fda78-1582">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="fda78-1582">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1583">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1583">Az.Websites</span></span>
* <span data-ttu-id="fda78-1584">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fda78-1584">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="fda78-1585">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="fda78-1585">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="fda78-1586">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="fda78-1586">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="fda78-1587">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1587">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1588">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1589">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="fda78-1589">Add support for profile cmdlets</span></span>
* <span data-ttu-id="fda78-1590">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="fda78-1590">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="fda78-1591">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fda78-1591">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="fda78-1592">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fda78-1592">Az.Advisor</span></span>
* <span data-ttu-id="fda78-1593">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="fda78-1593">GA release of Az.Advisor</span></span>
* <span data-ttu-id="fda78-1594">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="fda78-1594">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="fda78-1595">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1595">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-1596">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="fda78-1596">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="fda78-1597">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="fda78-1597">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="fda78-1598">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="fda78-1598">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="fda78-1599">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="fda78-1599">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="fda78-1600">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="fda78-1600">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="fda78-1601">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fda78-1601">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="fda78-1602">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="fda78-1602">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-1603">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1603">Az.Automation</span></span>
* <span data-ttu-id="fda78-1604">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fda78-1604">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1605">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1605">Az.Compute</span></span>
* <span data-ttu-id="fda78-1606">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1606">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-1607">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-1607">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-1608">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="fda78-1608">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fda78-1609">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fda78-1609">Az.EventGrid</span></span>
* <span data-ttu-id="fda78-1610">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="fda78-1610">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-1611">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1611">Az.IotHub</span></span>
* <span data-ttu-id="fda78-1612">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="fda78-1612">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1613">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1613">Az.Network</span></span>
* <span data-ttu-id="fda78-1614">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="fda78-1614">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="fda78-1615">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="fda78-1615">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-1616">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1616">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-1617">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="fda78-1617">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="fda78-1618">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="fda78-1618">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-1620">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fda78-1620">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1621">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1621">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1622">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="fda78-1622">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1623">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1623">Az.Resources</span></span>
    - <span data-ttu-id="fda78-1624">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="fda78-1624">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="fda78-1625">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="fda78-1625">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="fda78-1626">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1626">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="fda78-1627">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="fda78-1627">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-1628">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-1628">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-1629">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="fda78-1629">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1630">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1630">Az.Sql</span></span>
* <span data-ttu-id="fda78-1631">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="fda78-1631">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="fda78-1632">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fda78-1632">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="fda78-1633">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1633">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fda78-1634">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1634">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fda78-1635">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1635">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="fda78-1636">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1636">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fda78-1637">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1637">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="fda78-1638">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="fda78-1638">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="fda78-1639">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="fda78-1639">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1640">Az.Storage</span></span>
* <span data-ttu-id="fda78-1641">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1641">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="fda78-1642">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fda78-1642">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="fda78-1643">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="fda78-1643">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="fda78-1644">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="fda78-1644">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="fda78-1645">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1645">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="fda78-1646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1646">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="fda78-1647">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1647">Set-AzStorageAccount</span></span>
* <span data-ttu-id="fda78-1648">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="fda78-1648">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="fda78-1649">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fda78-1649">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="fda78-1650">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="fda78-1650">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="fda78-1651">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="fda78-1651">Az.StorageSync</span></span>
* <span data-ttu-id="fda78-1652">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="fda78-1652">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="fda78-1653">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1653">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-1654">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1654">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1655">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="fda78-1655">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="fda78-1656">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="fda78-1656">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="fda78-1657">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="fda78-1657">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="fda78-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fda78-1658">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="fda78-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="fda78-1659">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1660">Az.Compute</span></span>
* <span data-ttu-id="fda78-1661">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1661">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="fda78-1662">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="fda78-1662">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="fda78-1663">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fda78-1663">Az.Dns</span></span>
* <span data-ttu-id="fda78-1664">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1664">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fda78-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fda78-1665">Az.EventGrid</span></span>
* <span data-ttu-id="fda78-1666">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="fda78-1666">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="fda78-1667">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fda78-1667">New cmdlets:</span></span>
    - <span data-ttu-id="fda78-1668">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fda78-1668">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fda78-1669">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1669">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fda78-1670">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fda78-1670">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fda78-1671">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1671">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="fda78-1672">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="fda78-1672">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="fda78-1673">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1673">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fda78-1674">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1674">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fda78-1675">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1675">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="fda78-1676">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1676">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="fda78-1677">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1677">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="fda78-1678">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fda78-1678">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fda78-1679">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1679">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="fda78-1680">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fda78-1680">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="fda78-1681">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="fda78-1681">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="fda78-1682">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="fda78-1682">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="fda78-1683">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="fda78-1683">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="fda78-1684">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="fda78-1684">Updated cmdlets:</span></span>
    - <span data-ttu-id="fda78-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fda78-1685">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="fda78-1686">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1686">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fda78-1687">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1687">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="fda78-1688">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="fda78-1688">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="fda78-1689">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="fda78-1689">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="fda78-1690">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="fda78-1690">Event subscription expiration date,</span></span>
            - <span data-ttu-id="fda78-1691">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="fda78-1691">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="fda78-1692">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="fda78-1692">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="fda78-1693">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="fda78-1693">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="fda78-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="fda78-1694">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="fda78-1695">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="fda78-1695">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="fda78-1696">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fda78-1696">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="fda78-1697">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1697">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="fda78-1698">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="fda78-1698">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-1699">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-1699">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-1700">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1700">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="fda78-1701">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="fda78-1701">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="fda78-1702">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1702">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="fda78-1703">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="fda78-1703">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1704">Az.Network</span></span>
* <span data-ttu-id="fda78-1705">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="fda78-1705">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="fda78-1706">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1706">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="fda78-1707">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="fda78-1708">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fda78-1708">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="fda78-1709">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1709">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1710">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="fda78-1710">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="fda78-1711">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1711">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="fda78-1712">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1712">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1713">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1713">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fda78-1714">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1714">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fda78-1715">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fda78-1715">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="fda78-1716">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1716">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="fda78-1717">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1717">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="fda78-1718">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-1718">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="fda78-1719">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1719">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1720">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-1720">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fda78-1721">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-1721">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fda78-1722">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="fda78-1722">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="fda78-1723">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1723">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="fda78-1724">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fda78-1724">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="fda78-1725">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="fda78-1725">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="fda78-1726">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="fda78-1726">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="fda78-1727">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fda78-1727">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="fda78-1728">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="fda78-1728">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="fda78-1729">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fda78-1729">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="fda78-1730">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-1730">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="fda78-1731">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="fda78-1731">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="fda78-1732">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-1732">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="fda78-1733">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="fda78-1733">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="fda78-1734">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1734">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="fda78-1735">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1735">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="fda78-1736">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="fda78-1736">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="fda78-1737">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1737">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="fda78-1738">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="fda78-1738">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="fda78-1739">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="fda78-1739">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="fda78-1740">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="fda78-1740">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="fda78-1741">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="fda78-1741">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="fda78-1742">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fda78-1742">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="fda78-1743">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fda78-1743">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="fda78-1744">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1744">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fda78-1745">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1745">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="fda78-1746">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1746">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-1747">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1747">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-1748">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="fda78-1748">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1749">Az.Resources</span></span>
* <span data-ttu-id="fda78-1750">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="fda78-1750">Support for additional Template Export options</span></span>
    - <span data-ttu-id="fda78-1751">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1751">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fda78-1752">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1752">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="fda78-1753">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="fda78-1753">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-1754">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1754">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-1755">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="fda78-1755">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1756">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1756">Az.Sql</span></span>
* <span data-ttu-id="fda78-1757">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="fda78-1757">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="fda78-1758">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="fda78-1758">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="fda78-1759">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="fda78-1759">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="fda78-1760">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1760">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fda78-1761">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1761">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fda78-1762">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fda78-1762">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="fda78-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fda78-1763">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="fda78-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fda78-1764">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1765">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1765">Az.Storage</span></span>
* <span data-ttu-id="fda78-1766">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-1766">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="fda78-1767">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1767">New-AzStorageAccount</span></span>
* <span data-ttu-id="fda78-1768">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="fda78-1768">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="fda78-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-1769">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1770">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1770">Az.Websites</span></span>
* <span data-ttu-id="fda78-1771">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="fda78-1771">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="fda78-1772">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fda78-1772">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="fda78-1773">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1773">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="fda78-1774">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-1774">Az.Cdn</span></span>
* <span data-ttu-id="fda78-1775">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="fda78-1775">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1776">Az.Compute</span></span>
* <span data-ttu-id="fda78-1777">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="fda78-1777">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="fda78-1778">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fda78-1778">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-1779">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-1779">Az.EventHub</span></span>
* <span data-ttu-id="fda78-1780">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="fda78-1780">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="fda78-1781">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda78-1781">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1782">Az.Network</span></span>
* <span data-ttu-id="fda78-1783">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="fda78-1783">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="fda78-1784">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="fda78-1784">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-1785">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1785">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-1786">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="fda78-1786">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1787">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1787">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1788">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="fda78-1788">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-1789">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-1789">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-1790">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda78-1790">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-1791">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1791">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-1792">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="fda78-1792">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="fda78-1793">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1793">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1794">Az.Sql</span></span>
* <span data-ttu-id="fda78-1795">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="fda78-1795">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="fda78-1796">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-1796">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="fda78-1797">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="fda78-1797">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="fda78-1798">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="fda78-1798">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1799">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1799">Az.Websites</span></span>
* <span data-ttu-id="fda78-1800">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="fda78-1800">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="fda78-1801">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1801">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="fda78-1802">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1802">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-1803">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1803">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="fda78-1804">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1804">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="fda78-1805">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1805">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="fda78-1806">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="fda78-1806">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="fda78-1807">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1807">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="fda78-1808">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="fda78-1808">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="fda78-1809">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1809">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="fda78-1810">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1810">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="fda78-1811">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1811">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="fda78-1812">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="fda78-1812">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="fda78-1813">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1813">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="fda78-1814">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="fda78-1814">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="fda78-1815">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="fda78-1815">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="fda78-1816">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="fda78-1816">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="fda78-1817">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="fda78-1817">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="fda78-1818">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="fda78-1818">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="fda78-1819">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="fda78-1819">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="fda78-1820">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="fda78-1820">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="fda78-1821">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="fda78-1821">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="fda78-1822">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="fda78-1822">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="fda78-1823">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="fda78-1823">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="fda78-1824">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="fda78-1824">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="fda78-1825">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="fda78-1825">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="fda78-1826">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-1826">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="fda78-1827">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="fda78-1827">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="fda78-1828">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="fda78-1828">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="fda78-1829">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1829">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="fda78-1830">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fda78-1830">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="fda78-1831">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fda78-1831">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="fda78-1832">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="fda78-1832">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="fda78-1833">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="fda78-1833">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="fda78-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="fda78-1834">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="fda78-1835">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="fda78-1835">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="fda78-1836">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fda78-1836">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fda78-1837">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="fda78-1837">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="fda78-1838">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="fda78-1838">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="fda78-1839">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="fda78-1839">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="fda78-1840">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="fda78-1840">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="fda78-1841">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="fda78-1841">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="fda78-1842">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fda78-1842">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fda78-1843">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1843">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fda78-1844">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-1844">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="fda78-1845">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1845">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="fda78-1846">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="fda78-1846">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="fda78-1847">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="fda78-1847">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="fda78-1848">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1848">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="fda78-1849">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-1849">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="fda78-1850">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="fda78-1850">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="fda78-1851">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="fda78-1851">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="fda78-1852">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1852">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="fda78-1853">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="fda78-1853">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="fda78-1854">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="fda78-1854">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="fda78-1855">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="fda78-1855">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="fda78-1856">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="fda78-1856">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="fda78-1857">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="fda78-1857">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="fda78-1858">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="fda78-1858">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="fda78-1859">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="fda78-1859">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fda78-1860">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="fda78-1860">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fda78-1861">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="fda78-1861">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fda78-1862">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fda78-1862">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fda78-1863">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="fda78-1863">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="fda78-1864">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="fda78-1864">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="fda78-1865">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="fda78-1865">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="fda78-1866">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fda78-1866">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="fda78-1867">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="fda78-1867">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="fda78-1868">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="fda78-1868">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="fda78-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="fda78-1869">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="fda78-1870">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="fda78-1870">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="fda78-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="fda78-1871">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="fda78-1872">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-1872">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="fda78-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="fda78-1873">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="fda78-1874">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="fda78-1874">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="fda78-1875">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="fda78-1875">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="fda78-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="fda78-1876">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="fda78-1877">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="fda78-1877">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="fda78-1878">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="fda78-1878">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="fda78-1879">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="fda78-1879">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-1880">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1880">Az.Automation</span></span>
* <span data-ttu-id="fda78-1881">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="fda78-1881">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="fda78-1882">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="fda78-1882">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="fda78-1883">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="fda78-1883">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="fda78-1884">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="fda78-1884">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="fda78-1885">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="fda78-1885">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="fda78-1886">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="fda78-1886">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="fda78-1887">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="fda78-1887">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1888">Az.Compute</span></span>
* <span data-ttu-id="fda78-1889">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="fda78-1889">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="fda78-1890">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="fda78-1890">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-1891">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-1891">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-1892">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1892">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-1893">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-1893">Az.Monitor</span></span>
* <span data-ttu-id="fda78-1894">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-1894">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1895">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1895">Az.Network</span></span>
* <span data-ttu-id="fda78-1896">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="fda78-1896">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="fda78-1897">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fda78-1897">Updated cmdlet:</span></span>
        - <span data-ttu-id="fda78-1898">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-1898">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="fda78-1899">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fda78-1899">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-1900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-1900">Az.Resources</span></span>
* <span data-ttu-id="fda78-1901">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="fda78-1901">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-1902">Az.Sql</span></span>
* <span data-ttu-id="fda78-1903">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="fda78-1903">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="fda78-1904">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1904">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-1905">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-1905">Az.Accounts</span></span>
* <span data-ttu-id="fda78-1906">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="fda78-1906">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-1907">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1907">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-1908">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="fda78-1908">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="fda78-1909">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="fda78-1909">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-1910">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-1910">Az.Compute</span></span>
* <span data-ttu-id="fda78-1911">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="fda78-1911">Proximity placement group feature.</span></span>
    - <span data-ttu-id="fda78-1912">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1912">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="fda78-1913">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-1913">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="fda78-1914">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="fda78-1914">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="fda78-1915">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="fda78-1915">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="fda78-1916">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-1916">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="fda78-1917">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="fda78-1917">Breaking changes</span></span>
    - <span data-ttu-id="fda78-1918">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="fda78-1918">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="fda78-1919">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="fda78-1919">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="fda78-1920">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="fda78-1920">Az.DeploymentManager</span></span>
* <span data-ttu-id="fda78-1921">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1921">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="fda78-1922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="fda78-1922">Az.Dns</span></span>
* <span data-ttu-id="fda78-1923">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="fda78-1923">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="fda78-1924">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="fda78-1924">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="fda78-1925">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="fda78-1925">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="fda78-1926">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-1926">Az.FrontDoor</span></span>
* <span data-ttu-id="fda78-1927">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-1927">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="fda78-1928">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="fda78-1928">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="fda78-1929">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-1929">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-1930">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fda78-1930">Removed two cmdlets:</span></span>
    - <span data-ttu-id="fda78-1931">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fda78-1931">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="fda78-1932">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fda78-1932">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fda78-1933">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fda78-1933">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="fda78-1934">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="fda78-1934">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="fda78-1935">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="fda78-1935">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="fda78-1936">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="fda78-1936">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-1937">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-1937">Az.Monitor</span></span>
* <span data-ttu-id="fda78-1938">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="fda78-1938">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="fda78-1939">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="fda78-1939">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="fda78-1940">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-1940">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="fda78-1941">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="fda78-1941">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="fda78-1942">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="fda78-1942">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="fda78-1943">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="fda78-1943">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="fda78-1944">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="fda78-1944">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="fda78-1945">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1945">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fda78-1946">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1946">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fda78-1947">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1947">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fda78-1948">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1948">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fda78-1949">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fda78-1949">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="fda78-1950">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="fda78-1950">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="fda78-1951">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="fda78-1951">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-1952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1952">Az.Network</span></span>
* <span data-ttu-id="fda78-1953">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="fda78-1953">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="fda78-1954">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="fda78-1954">New cmdlets</span></span>
        - <span data-ttu-id="fda78-1955">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1955">New-AzNatGateway</span></span>
        - <span data-ttu-id="fda78-1956">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1956">Get-AzNatGateway</span></span>
        - <span data-ttu-id="fda78-1957">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1957">Set-AzNatGateway</span></span>
        - <span data-ttu-id="fda78-1958">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-1958">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="fda78-1959">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="fda78-1959">Updated cmdlets</span></span>
        - <span data-ttu-id="fda78-1960">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fda78-1960">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="fda78-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="fda78-1961">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="fda78-1962">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="fda78-1962">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="fda78-1963">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1963">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="fda78-1964">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="fda78-1964">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-1965">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-1965">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-1966">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="fda78-1966">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="fda78-1967">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="fda78-1967">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="fda78-1968">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="fda78-1968">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-1969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-1969">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-1970">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fda78-1970">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="fda78-1971">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fda78-1971">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="fda78-1972">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fda78-1972">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="fda78-1973">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-1973">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="fda78-1974">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fda78-1974">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="fda78-1975">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="fda78-1975">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="fda78-1976">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fda78-1976">Az.Relay</span></span>
* <span data-ttu-id="fda78-1977">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="fda78-1977">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-1978">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-1978">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-1979">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="fda78-1979">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-1980">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-1980">Az.Storage</span></span>
* <span data-ttu-id="fda78-1981">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="fda78-1981">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="fda78-1982">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="fda78-1982">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="fda78-1983">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="fda78-1983">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="fda78-1984">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1984">New-AzStorageAccount</span></span>
* <span data-ttu-id="fda78-1985">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="fda78-1985">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="fda78-1986">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1986">New-AzStorageAccount</span></span>
    - <span data-ttu-id="fda78-1987">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1987">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="fda78-1988">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-1988">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-1989">Az.Websites</span></span>
* <span data-ttu-id="fda78-1990">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fda78-1990">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="fda78-1991">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="fda78-1991">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="fda78-1992">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-1992">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-1993">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-1993">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-1994">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="fda78-1994">General availability of `Az` module</span></span>
* <span data-ttu-id="fda78-1995">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fda78-1995">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fda78-1996">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fda78-1996">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fda78-1997">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-1997">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fda78-1998">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="fda78-1998">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fda78-1999">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-1999">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fda78-2000">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="fda78-2000">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-2001">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2001">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2002">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="fda78-2002">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="fda78-2003">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-2003">Az.Batch</span></span>
* <span data-ttu-id="fda78-2004">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2004">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-2005">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-2005">Az.Cdn</span></span>
* <span data-ttu-id="fda78-2006">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2006">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-2008">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2008">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2009">Az.Compute</span></span>
* <span data-ttu-id="fda78-2010">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="fda78-2010">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="fda78-2011">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2011">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2012">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="fda78-2012">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-2013">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-2014">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fda78-2014">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2015">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2015">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2016">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2016">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fda78-2017">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fda78-2017">Az.EventGrid</span></span>
* <span data-ttu-id="fda78-2018">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="fda78-2018">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-2019">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2019">Az.EventHub</span></span>
* <span data-ttu-id="fda78-2020">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="fda78-2020">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="fda78-2021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fda78-2021">Az.HDInsight</span></span>
* <span data-ttu-id="fda78-2022">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2022">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-2023">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2023">Az.IotHub</span></span>
* <span data-ttu-id="fda78-2024">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2024">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-2025">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2025">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-2026">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2026">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2027">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="fda78-2027">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="fda78-2028">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fda78-2028">Az.MachineLearning</span></span>
* <span data-ttu-id="fda78-2029">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2029">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="fda78-2030">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fda78-2030">Az.Media</span></span>
* <span data-ttu-id="fda78-2031">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2031">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-2032">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-2032">Az.Monitor</span></span>
  * <span data-ttu-id="fda78-2033">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="fda78-2033">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="fda78-2034">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="fda78-2034">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="fda78-2035">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="fda78-2035">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="fda78-2036">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fda78-2036">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fda78-2037">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fda78-2037">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="fda78-2038">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="fda78-2038">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="fda78-2039">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="fda78-2039">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2040">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2040">Az.Network</span></span>
* <span data-ttu-id="fda78-2041">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2041">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2042">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="fda78-2042">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="fda78-2043">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fda78-2043">Az.NotificationHubs</span></span>
* <span data-ttu-id="fda78-2044">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2044">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-2045">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-2045">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-2046">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2046">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="fda78-2047">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fda78-2047">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="fda78-2048">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2048">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-2050">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2050">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2051">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2051">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="fda78-2052">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="fda78-2052">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="fda78-2053">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="fda78-2053">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fda78-2054">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fda78-2054">Az.RedisCache</span></span>
* <span data-ttu-id="fda78-2055">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2055">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2056">Az.Resources</span></span>
* <span data-ttu-id="fda78-2057">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="fda78-2057">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2058">Az.Sql</span></span>
* <span data-ttu-id="fda78-2059">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="fda78-2059">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="fda78-2060">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2060">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2061">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="fda78-2061">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="fda78-2062">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="fda78-2062">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="fda78-2063">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="fda78-2063">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="fda78-2064">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="fda78-2064">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="fda78-2065">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="fda78-2065">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2066">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2066">Az.Websites</span></span>
* <span data-ttu-id="fda78-2067">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="fda78-2067">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="fda78-2068">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2068">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="fda78-2069">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="fda78-2069">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="fda78-2070">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="fda78-2070">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="fda78-2071">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2071">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-2072">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-2072">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-2073">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="fda78-2073">General availability of `Az` module</span></span>
* <span data-ttu-id="fda78-2074">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fda78-2074">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fda78-2075">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fda78-2075">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fda78-2076">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2076">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fda78-2077">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="fda78-2077">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fda78-2078">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2078">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fda78-2079">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="fda78-2079">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="fda78-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2080">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2081">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="fda78-2081">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fda78-2082">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2082">Az.AnalysisServices</span></span>
* <span data-ttu-id="fda78-2083">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="fda78-2083">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="fda78-2084">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="fda78-2084">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-2085">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2085">Az.Automation</span></span>
* <span data-ttu-id="fda78-2086">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="fda78-2086">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="fda78-2087">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="fda78-2087">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="fda78-2088">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2088">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2089">Az.Compute</span></span>
* <span data-ttu-id="fda78-2090">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2090">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="fda78-2091">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="fda78-2091">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="fda78-2092">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2092">Az.ContainerInstance</span></span>
* <span data-ttu-id="fda78-2093">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="fda78-2093">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-2094">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-2094">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-2095">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="fda78-2095">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="fda78-2096">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fda78-2096">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2097">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2097">Az.Resources</span></span>
* <span data-ttu-id="fda78-2098">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="fda78-2098">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="fda78-2099">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-2099">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="fda78-2100">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="fda78-2100">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="fda78-2101">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fda78-2101">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="fda78-2102">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="fda78-2102">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="fda78-2103">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="fda78-2103">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2104">Az.Sql</span></span>
* <span data-ttu-id="fda78-2105">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="fda78-2105">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-2106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2106">Az.Storage</span></span>
* <span data-ttu-id="fda78-2107">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2107">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="fda78-2108">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fda78-2108">New-AzStorageContext</span></span>
* <span data-ttu-id="fda78-2109">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fda78-2109">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="fda78-2110">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fda78-2110">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fda78-2111">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fda78-2111">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="fda78-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2112">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="fda78-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2113">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="fda78-2114">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="fda78-2114">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="fda78-2115">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fda78-2115">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fda78-2116">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fda78-2116">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="fda78-2117">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fda78-2117">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="fda78-2118">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fda78-2118">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="fda78-2119">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2119">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="fda78-2120">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="fda78-2120">Highlights since the last major release</span></span>
* <span data-ttu-id="fda78-2121">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="fda78-2121">General availability of `Az` module</span></span>
* <span data-ttu-id="fda78-2122">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="fda78-2122">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="fda78-2123">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="fda78-2123">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="fda78-2124">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2124">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="fda78-2125">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="fda78-2125">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fda78-2126">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2126">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="fda78-2127">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="fda78-2127">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-2128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2128">Az.Automation</span></span>
* <span data-ttu-id="fda78-2129">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="fda78-2129">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="fda78-2130">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="fda78-2130">Dynamic grouping</span></span>
    * <span data-ttu-id="fda78-2131">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="fda78-2131">Pre-Post script</span></span>
    * <span data-ttu-id="fda78-2132">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="fda78-2132">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2133">Az.Compute</span></span>
* <span data-ttu-id="fda78-2134">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="fda78-2134">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="fda78-2135">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="fda78-2135">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-2136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2136">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-2137">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2137">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2138">Az.Network</span></span>
* <span data-ttu-id="fda78-2139">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2139">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="fda78-2140">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="fda78-2140">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2141">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-2142">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="fda78-2142">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="fda78-2143">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="fda78-2143">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2144">Az.Resources</span></span>
* <span data-ttu-id="fda78-2145">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fda78-2145">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="fda78-2146">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="fda78-2146">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2147">Az.Sql</span></span>
* <span data-ttu-id="fda78-2148">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="fda78-2148">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-2149">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2149">Az.Storage</span></span>
* <span data-ttu-id="fda78-2150">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-2150">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="fda78-2151">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2151">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fda78-2152">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2152">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fda78-2153">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2153">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="fda78-2154">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fda78-2154">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="fda78-2155">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fda78-2155">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="fda78-2156">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fda78-2156">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2157">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2157">Az.Websites</span></span>
* <span data-ttu-id="fda78-2158">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="fda78-2158">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="fda78-2159">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2159">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-2160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2160">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2161">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="fda78-2161">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="fda78-2162">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2162">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-2163">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2163">Az.Automation</span></span>
* <span data-ttu-id="fda78-2164">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2164">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="fda78-2165">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="fda78-2165">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="fda78-2166">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="fda78-2166">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-2167">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-2167">Az.Cdn</span></span>
* <span data-ttu-id="fda78-2168">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="fda78-2168">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2169">Az.Compute</span></span>
* <span data-ttu-id="fda78-2170">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="fda78-2170">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-2171">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-2171">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-2172">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="fda78-2172">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fda78-2173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fda78-2173">Az.LogicApp</span></span>
* <span data-ttu-id="fda78-2174">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="fda78-2174">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2175">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2175">Az.Network</span></span>
* <span data-ttu-id="fda78-2176">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2176">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2177">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-2178">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2178">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="fda78-2179">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="fda78-2179">SDK Update</span></span>
* <span data-ttu-id="fda78-2180">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fda78-2180">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="fda78-2181">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fda78-2181">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2182">Az.Resources</span></span>
* <span data-ttu-id="fda78-2183">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="fda78-2183">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="fda78-2184">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="fda78-2184">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="fda78-2185">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="fda78-2185">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="fda78-2186">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="fda78-2186">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="fda78-2187">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="fda78-2187">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="fda78-2188">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="fda78-2188">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2189">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2189">Az.Sql</span></span>
* <span data-ttu-id="fda78-2190">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="fda78-2190">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="fda78-2191">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="fda78-2191">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-2192">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2192">Az.Storage</span></span>
* <span data-ttu-id="fda78-2193">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2193">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="fda78-2194">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2194">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="fda78-2195">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2195">Az.AnalysisServices</span></span>
* <span data-ttu-id="fda78-2196">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2196">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-2197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2197">Az.Automation</span></span>
* <span data-ttu-id="fda78-2198">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2198">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="fda78-2199">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2199">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="fda78-2200">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2200">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-2201">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2201">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-2202">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="fda78-2202">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2203">Az.Compute</span></span>
* <span data-ttu-id="fda78-2204">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="fda78-2204">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="fda78-2205">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="fda78-2205">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="fda78-2206">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="fda78-2206">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="fda78-2207">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="fda78-2207">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2208">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2209">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="fda78-2209">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="fda78-2210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2210">Az.EventHub</span></span>
* <span data-ttu-id="fda78-2211">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2211">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-2212">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2212">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-2213">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fda78-2213">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fda78-2214">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fda78-2214">Az.LogicApp</span></span>
* <span data-ttu-id="fda78-2215">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="fda78-2215">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="fda78-2216">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="fda78-2216">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="fda78-2217">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="fda78-2217">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="fda78-2218">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fda78-2218">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fda78-2219">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fda78-2219">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fda78-2220">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fda78-2220">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="fda78-2221">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="fda78-2221">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="fda78-2222">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="fda78-2222">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="fda78-2223">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2223">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fda78-2224">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2224">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fda78-2225">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2225">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="fda78-2226">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2226">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="fda78-2227">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="fda78-2227">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="fda78-2228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-2228">Az.Monitor</span></span>
* <span data-ttu-id="fda78-2229">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="fda78-2229">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2230">Az.Network</span></span>
* <span data-ttu-id="fda78-2231">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fda78-2231">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-2232">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-2232">Az.OperationalInsights</span></span>
* <span data-ttu-id="fda78-2233">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="fda78-2233">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="fda78-2234">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="fda78-2234">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="fda78-2235">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="fda78-2235">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2236">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2236">Az.Resources</span></span>
* <span data-ttu-id="fda78-2237">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fda78-2237">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fda78-2238">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fda78-2238">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="fda78-2239">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="fda78-2239">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="fda78-2240">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="fda78-2240">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2241">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2241">Az.Sql</span></span>
* <span data-ttu-id="fda78-2242">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="fda78-2242">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="fda78-2243">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="fda78-2243">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2244">Az.Websites</span></span>
* <span data-ttu-id="fda78-2245">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="fda78-2245">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="fda78-2246">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2246">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-2247">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2247">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2248">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fda78-2248">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fda78-2249">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2249">Az.AnalysisServices</span></span>
<span data-ttu-id="fda78-2250">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="fda78-2250">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2251">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2251">Az.Compute</span></span>
* <span data-ttu-id="fda78-2252">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="fda78-2252">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="fda78-2253">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="fda78-2253">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="fda78-2254">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="fda78-2254">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2255">Az.RecoveryServices</span></span>
<span data-ttu-id="fda78-2256">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="fda78-2256">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2257">Az.Resources</span></span>
* <span data-ttu-id="fda78-2258">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="fda78-2258">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="fda78-2259">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="fda78-2259">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="fda78-2260">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="fda78-2260">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="fda78-2261">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="fda78-2261">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2262">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2262">Az.Sql</span></span>
* <span data-ttu-id="fda78-2263">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fda78-2263">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="fda78-2264">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="fda78-2264">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="fda78-2265">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="fda78-2265">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="fda78-2266">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2266">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-2267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2267">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2268">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="fda78-2268">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="fda78-2269">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2269">Az.AnalysisServices</span></span>
* <span data-ttu-id="fda78-2270">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-2270">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2271">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2271">Az.RecoveryServices</span></span>
* <span data-ttu-id="fda78-2272">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-2272">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="fda78-2273">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2273">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-2274">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2274">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2275">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="fda78-2275">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="fda78-2276">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2276">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fda78-2277">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="fda78-2277">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="fda78-2278">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="fda78-2278">Az.Aks</span></span>
* <span data-ttu-id="fda78-2279">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2279">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="fda78-2280">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2280">Az.Automation</span></span>
* <span data-ttu-id="fda78-2281">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="fda78-2281">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="fda78-2282">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2282">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="fda78-2283">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="fda78-2283">Az.Cdn</span></span>
* <span data-ttu-id="fda78-2284">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2284">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2285">Az.Compute</span></span>
* <span data-ttu-id="fda78-2286">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="fda78-2286">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="fda78-2287">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fda78-2287">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="fda78-2288">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="fda78-2288">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="fda78-2289">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fda78-2289">Az.ContainerRegistry</span></span>
* <span data-ttu-id="fda78-2290">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2290">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="fda78-2291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="fda78-2291">Az.DataFactory</span></span>
* <span data-ttu-id="fda78-2292">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="fda78-2292">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2293">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2293">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2294">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="fda78-2294">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="fda78-2295">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="fda78-2295">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="fda78-2296">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2296">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-2297">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2297">Az.IotHub</span></span>
* <span data-ttu-id="fda78-2298">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fda78-2298">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="fda78-2299">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2299">Az.KeyVault</span></span>
* <span data-ttu-id="fda78-2300">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2300">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2301">Az.Network</span></span>
* <span data-ttu-id="fda78-2302">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2302">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2303">Az.Resources</span></span>
* <span data-ttu-id="fda78-2304">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="fda78-2304">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="fda78-2305">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fda78-2305">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="fda78-2306">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="fda78-2306">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="fda78-2307">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="fda78-2307">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="fda78-2308">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="fda78-2308">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="fda78-2309">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="fda78-2309">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="fda78-2310">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="fda78-2310">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-2311">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-2311">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-2312">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="fda78-2312">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="fda78-2313">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="fda78-2313">Fix some error messages.</span></span>
* <span data-ttu-id="fda78-2314">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="fda78-2314">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="fda78-2315">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="fda78-2315">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fda78-2316">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fda78-2316">Az.SignalR</span></span>
* <span data-ttu-id="fda78-2317">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2317">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2318">Az.Sql</span></span>
* <span data-ttu-id="fda78-2319">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2319">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fda78-2320">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fda78-2320">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="fda78-2321">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="fda78-2321">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="fda78-2322">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="fda78-2322">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2323">Az.Storage</span></span>
* <span data-ttu-id="fda78-2324">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2324">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fda78-2325">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2325">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="fda78-2326">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="fda78-2326">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="fda78-2327">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="fda78-2327">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="fda78-2328">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fda78-2328">Az.TrafficManager</span></span>
* <span data-ttu-id="fda78-2329">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2329">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2330">Az.Websites</span></span>
* <span data-ttu-id="fda78-2331">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="fda78-2331">Update incorrect online help URLs</span></span>
* <span data-ttu-id="fda78-2332">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="fda78-2332">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="fda78-2333">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="fda78-2333">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="fda78-2334">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="fda78-2334">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="fda78-2335">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2335">Az.Accounts</span></span>
* <span data-ttu-id="fda78-2336">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="fda78-2336">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2337">Az.Compute</span></span>
* <span data-ttu-id="fda78-2338">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="fda78-2338">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="fda78-2339">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="fda78-2339">Updated the description of ID in help files</span></span>
* <span data-ttu-id="fda78-2340">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2340">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2341">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2342">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="fda78-2342">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="fda78-2343">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="fda78-2343">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="fda78-2344">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fda78-2344">Az.EventGrid</span></span>
* <span data-ttu-id="fda78-2345">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="fda78-2345">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="fda78-2346">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="fda78-2346">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="fda78-2347">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="fda78-2347">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fda78-2348">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="fda78-2348">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fda78-2349">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="fda78-2349">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fda78-2350">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="fda78-2350">Dead letter endpoint.</span></span>
    - <span data-ttu-id="fda78-2351">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="fda78-2351">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="fda78-2352">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="fda78-2352">Event Time-To-Live,</span></span>
        - <span data-ttu-id="fda78-2353">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="fda78-2353">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="fda78-2354">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="fda78-2354">Dead letter endpoint.</span></span>
* <span data-ttu-id="fda78-2355">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="fda78-2355">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="fda78-2356">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="fda78-2356">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="fda78-2357">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2357">Az.IotHub</span></span>
* <span data-ttu-id="fda78-2358">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="fda78-2358">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="fda78-2359">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fda78-2359">Az.LogicApp</span></span>
* <span data-ttu-id="fda78-2360">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="fda78-2360">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2361">Az.Resources</span></span>
* <span data-ttu-id="fda78-2362">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="fda78-2362">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="fda78-2363">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="fda78-2363">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="fda78-2364">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fda78-2364">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fda78-2365">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="fda78-2365">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="fda78-2366">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="fda78-2366">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="fda78-2367">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="fda78-2367">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="fda78-2368">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="fda78-2368">Az.SignalR</span></span>
* <span data-ttu-id="fda78-2369">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2369">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2370">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2370">Az.Sql</span></span>
* <span data-ttu-id="fda78-2371">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="fda78-2371">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="fda78-2372">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2372">Az.Storage</span></span>
* <span data-ttu-id="fda78-2373">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="fda78-2373">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="fda78-2374">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fda78-2374">New-AzStorageContext</span></span>
* <span data-ttu-id="fda78-2375">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="fda78-2375">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="fda78-2376">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fda78-2376">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2377">Az.Websites</span></span>
* <span data-ttu-id="fda78-2378">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="fda78-2378">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="fda78-2379">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2379">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="fda78-2380">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2380">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="fda78-2381">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-2381">General</span></span>

- <span data-ttu-id="fda78-2382">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="fda78-2382">General Availability of Az Module</span></span>
- <span data-ttu-id="fda78-2383">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="fda78-2383">Online help for each module</span></span>
- <span data-ttu-id="fda78-2384">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="fda78-2384">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="fda78-2385">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="fda78-2385">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="fda78-2386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2386">Az.Accounts</span></span>
- <span data-ttu-id="fda78-2387">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fda78-2387">Changed from Az.Profile</span></span>
- <span data-ttu-id="fda78-2388">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="fda78-2388">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fda78-2389">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-2389">Az.ApiManagement</span></span>
- <span data-ttu-id="fda78-2390">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="fda78-2390">Fixes for #7002</span></span>
- <span data-ttu-id="fda78-2391">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2391">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="fda78-2392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="fda78-2392">Az.Batch</span></span>
- <span data-ttu-id="fda78-2393">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="fda78-2393">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="fda78-2394">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="fda78-2394">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="fda78-2395">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2395">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="fda78-2396">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="fda78-2396">Az.Billing</span></span>
- <span data-ttu-id="fda78-2397">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2397">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="fda78-2398">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2398">Az.CognitivServices</span></span>
- <span data-ttu-id="fda78-2399">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2399">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="fda78-2400">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="fda78-2400">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fda78-2401">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2401">Az.ContainerInstance</span></span>
- <span data-ttu-id="fda78-2402">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="fda78-2402">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="fda78-2403">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fda78-2403">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="fda78-2404">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2404">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2405">Az.DataLakeStore</span></span>
- <span data-ttu-id="fda78-2406">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2406">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="fda78-2407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="fda78-2407">Az.Monitor</span></span>
- <span data-ttu-id="fda78-2408">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2408">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="fda78-2409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fda78-2409">Az.KeyVault</span></span>
- <span data-ttu-id="fda78-2410">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="fda78-2410">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="fda78-2411">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fda78-2411">Az.MachineLearning</span></span>
- <span data-ttu-id="fda78-2412">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fda78-2412">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="fda78-2413">Az.Media</span><span class="sxs-lookup"><span data-stu-id="fda78-2413">Az.Media</span></span>
- <span data-ttu-id="fda78-2414">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="fda78-2414">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fda78-2415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2415">Az.Network</span></span>
<span data-ttu-id="fda78-2416">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fda78-2416">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="fda78-2417">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="fda78-2417">New cmdlets added:</span></span>
        - <span data-ttu-id="fda78-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2418">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2419">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2420">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2421">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2422">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2423">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="fda78-2423">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="fda78-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2424">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="fda78-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda78-2425">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="fda78-2426">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda78-2426">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="fda78-2427">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda78-2427">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="fda78-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fda78-2428">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fda78-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="fda78-2429">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="fda78-2430">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2430">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="fda78-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2431">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="fda78-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="fda78-2432">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="fda78-2433">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="fda78-2433">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="fda78-2434">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fda78-2434">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fda78-2435">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fda78-2435">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="fda78-2436">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fda78-2436">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="fda78-2437">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fda78-2437">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="fda78-2438">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2438">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="fda78-2439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-2439">Az.OperationalInsights</span></span>
- <span data-ttu-id="fda78-2440">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2440">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="fda78-2441">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fda78-2441">Az.Profile</span></span>
- <span data-ttu-id="fda78-2442">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="fda78-2442">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2443">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2443">Az.RecoveryServices</span></span>
- <span data-ttu-id="fda78-2444">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2444">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="fda78-2445">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2445">Az.Resources</span></span>
- <span data-ttu-id="fda78-2446">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2446">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fda78-2447">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-2447">Az.ServiceFabric</span></span>
- <span data-ttu-id="fda78-2448">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="fda78-2448">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="fda78-2449">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2449">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="fda78-2450">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fda78-2450">Az.SIgnalR</span></span>
- <span data-ttu-id="fda78-2451">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="fda78-2451">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="fda78-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2452">Az.Sql</span></span>
- <span data-ttu-id="fda78-2453">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="fda78-2453">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="fda78-2454">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="fda78-2454">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="fda78-2455">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2455">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="fda78-2456">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2456">Az.Storage</span></span>
- <span data-ttu-id="fda78-2457">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2457">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fda78-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2458">Az.Websites</span></span>
- <span data-ttu-id="fda78-2459">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="fda78-2459">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="fda78-2460">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2460">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="fda78-2461">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-2461">General</span></span>

* <span data-ttu-id="fda78-2462">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="fda78-2462">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="fda78-2463">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2463">Az.Compute</span></span>

* <span data-ttu-id="fda78-2464">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="fda78-2464">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2465">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2465">Az.DataLakeStore</span></span>

* <span data-ttu-id="fda78-2466">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="fda78-2466">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="fda78-2467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="fda78-2467">Az.FrontDoor</span></span>

* <span data-ttu-id="fda78-2468">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="fda78-2468">Fixed some broken links</span></span>
    - <span data-ttu-id="fda78-2469">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="fda78-2469">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="fda78-2470">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="fda78-2470">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="fda78-2471">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2471">Az.RecoveryServices</span></span>

* <span data-ttu-id="fda78-2472">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2472">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="fda78-2473">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="fda78-2473">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="fda78-2474">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2474">Az.Resources</span></span>

* <span data-ttu-id="fda78-2475">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="fda78-2475">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="fda78-2476">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="fda78-2476">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="fda78-2477">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2477">Az.Sql</span></span>

* <span data-ttu-id="fda78-2478">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="fda78-2478">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="fda78-2479">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="fda78-2479">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="fda78-2480">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="fda78-2480">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="fda78-2481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2481">Az.Storage</span></span>

* <span data-ttu-id="fda78-2482">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2482">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="fda78-2483">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="fda78-2483">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="fda78-2484">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-2484">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fda78-2485">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="fda78-2485">Support Static Website configuration</span></span>
    - <span data-ttu-id="fda78-2486">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fda78-2486">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="fda78-2487">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="fda78-2487">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="fda78-2488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2488">Az.Websites</span></span>

* <span data-ttu-id="fda78-2489">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fda78-2489">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="fda78-2490">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="fda78-2490">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="fda78-2491">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fda78-2491">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="fda78-2492">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2492">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="fda78-2493">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fda78-2493">Az.ApiManagement</span></span>
* <span data-ttu-id="fda78-2494">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="fda78-2494">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="fda78-2495">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="fda78-2495">Az.Automation</span></span>
* <span data-ttu-id="fda78-2496">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="fda78-2496">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fda78-2497">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-2497">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fda78-2498">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-2498">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fda78-2499">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="fda78-2499">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fda78-2500">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="fda78-2500">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="fda78-2501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2501">Az.Compute</span></span>
* <span data-ttu-id="fda78-2502">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="fda78-2502">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fda78-2503">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="fda78-2503">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="fda78-2504">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2504">Az.ContainerInstance</span></span>
* <span data-ttu-id="fda78-2505">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="fda78-2505">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="fda78-2506">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fda78-2506">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="fda78-2507">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="fda78-2507">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="fda78-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2508">Az.Network</span></span>
* <span data-ttu-id="fda78-2509">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-2509">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fda78-2510">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="fda78-2510">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fda78-2511">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="fda78-2511">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="fda78-2512">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fda78-2512">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="fda78-2513">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fda78-2513">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fda78-2514">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="fda78-2514">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fda78-2515">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="fda78-2515">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="fda78-2516">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fda78-2516">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fda78-2517">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fda78-2517">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fda78-2518">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="fda78-2518">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="fda78-2519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="fda78-2519">Az.Relay</span></span>
* <span data-ttu-id="fda78-2520">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fda78-2520">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="fda78-2521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2521">Az.Resources</span></span>
* <span data-ttu-id="fda78-2522">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="fda78-2522">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="fda78-2523">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="fda78-2523">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fda78-2524">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="fda78-2524">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="fda78-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-2526">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="fda78-2526">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="fda78-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2527">Az.Sql</span></span>
* <span data-ttu-id="fda78-2528">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="fda78-2528">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fda78-2529">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2529">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fda78-2530">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2530">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fda78-2531">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2531">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fda78-2532">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fda78-2532">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fda78-2533">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fda78-2533">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fda78-2534">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fda78-2534">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fda78-2535">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fda78-2535">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fda78-2536">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fda78-2536">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fda78-2537">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fda78-2537">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fda78-2538">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="fda78-2538">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fda78-2539">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="fda78-2539">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fda78-2540">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fda78-2540">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fda78-2541">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fda78-2541">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fda78-2542">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fda78-2542">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fda78-2543">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fda78-2543">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fda78-2544">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fda78-2544">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="fda78-2545">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2545">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fda78-2546">Geral</span><span class="sxs-lookup"><span data-stu-id="fda78-2546">General</span></span>
* <span data-ttu-id="fda78-2547">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="fda78-2547">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="fda78-2548">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fda78-2548">Az.Profile</span></span>
* <span data-ttu-id="fda78-2549">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fda78-2549">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fda78-2550">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="fda78-2550">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fda78-2551">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="fda78-2551">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="fda78-2552">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="fda78-2552">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fda78-2553">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="fda78-2553">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fda78-2554">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="fda78-2554">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fda78-2555">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="fda78-2555">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-2556">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2556">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-2557">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="fda78-2557">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2558">Az.Compute</span></span>
* <span data-ttu-id="fda78-2559">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fda78-2559">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fda78-2560">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="fda78-2560">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fda78-2561">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="fda78-2561">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2562">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2563">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="fda78-2563">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fda78-2564">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="fda78-2564">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="fda78-2565">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="fda78-2565">Az.Insights</span></span>
* <span data-ttu-id="fda78-2566">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="fda78-2566">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fda78-2567">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="fda78-2567">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fda78-2568">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="fda78-2568">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fda78-2569">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="fda78-2569">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2570">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2570">Az.Network</span></span>
* <span data-ttu-id="fda78-2571">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="fda78-2571">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fda78-2572">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-2572">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fda78-2573">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fda78-2573">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fda78-2574">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fda78-2574">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fda78-2575">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fda78-2575">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fda78-2576">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fda78-2576">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fda78-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fda78-2577">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="fda78-2578">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fda78-2578">Az.PolicyInsights</span></span>
* <span data-ttu-id="fda78-2579">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="fda78-2579">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2580">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2580">Az.Resources</span></span>
* <span data-ttu-id="fda78-2581">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="fda78-2581">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fda78-2582">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="fda78-2582">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="fda78-2583">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fda78-2583">Az.ServiceBus</span></span>
* <span data-ttu-id="fda78-2584">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="fda78-2584">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="fda78-2585">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fda78-2585">Az.ServiceFabric</span></span>
* <span data-ttu-id="fda78-2586">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="fda78-2586">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fda78-2587">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="fda78-2587">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fda78-2588">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="fda78-2588">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fda78-2589">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="fda78-2589">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fda78-2590">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="fda78-2590">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="fda78-2591">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2591">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="fda78-2592">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="fda78-2592">Az.Profile</span></span>
* <span data-ttu-id="fda78-2593">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="fda78-2593">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="fda78-2594">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fda78-2594">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2595">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2595">Az.Compute</span></span>
* <span data-ttu-id="fda78-2596">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="fda78-2596">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="fda78-2597">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fda78-2597">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="fda78-2598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fda78-2598">Az.DataLakeStore</span></span>
* <span data-ttu-id="fda78-2599">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="fda78-2599">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fda78-2600">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fda78-2600">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fda78-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="fda78-2601">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fda78-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="fda78-2602">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fda78-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fda78-2603">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2604">Az.Network</span></span>
* <span data-ttu-id="fda78-2605">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="fda78-2605">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fda78-2606">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fda78-2606">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2607">Az.Resources</span></span>
* <span data-ttu-id="fda78-2608">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="fda78-2608">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fda78-2609">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="fda78-2609">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="fda78-2610">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2610">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fda78-2611">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fda78-2611">Azure.Storage</span></span>
* <span data-ttu-id="fda78-2612">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="fda78-2612">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fda78-2613">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-2613">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fda78-2614">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fda78-2614">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="fda78-2615">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="fda78-2615">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fda78-2616">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fda78-2616">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="fda78-2617">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fda78-2617">Az.CognitiveServices</span></span>
* <span data-ttu-id="fda78-2618">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="fda78-2618">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="fda78-2619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fda78-2619">Az.Compute</span></span>
* <span data-ttu-id="fda78-2620">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="fda78-2620">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fda78-2621">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="fda78-2621">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="fda78-2622">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="fda78-2622">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="fda78-2623">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fda78-2623">Az.DataFactoryV2</span></span>
* <span data-ttu-id="fda78-2624">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="fda78-2624">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="fda78-2625">Az.Network</span><span class="sxs-lookup"><span data-stu-id="fda78-2625">Az.Network</span></span>
* <span data-ttu-id="fda78-2626">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="fda78-2626">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fda78-2627">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="fda78-2627">new cmdlets added</span></span>
    - <span data-ttu-id="fda78-2628">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fda78-2628">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="fda78-2629">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fda78-2629">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="fda78-2630">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fda78-2630">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="fda78-2631">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fda78-2631">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="fda78-2632">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2632">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="fda78-2633">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2633">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fda78-2634">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="fda78-2634">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fda78-2635">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fda78-2635">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="fda78-2636">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fda78-2636">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="fda78-2637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fda78-2637">Az.RedisCache</span></span>
* <span data-ttu-id="fda78-2638">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="fda78-2638">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fda78-2639">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="fda78-2639">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="fda78-2640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="fda78-2640">Az.Resources</span></span>
* <span data-ttu-id="fda78-2641">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fda78-2641">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="fda78-2642">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="fda78-2642">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="fda78-2643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="fda78-2643">Az.Sql</span></span>
* <span data-ttu-id="fda78-2644">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="fda78-2644">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="fda78-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="fda78-2645">Az.Websites</span></span>
* <span data-ttu-id="fda78-2646">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="fda78-2646">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fda78-2647">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="fda78-2647">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="fda78-2648">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="fda78-2648">0.2.0 - September 2018</span></span>
 <span data-ttu-id="fda78-2649">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="fda78-2649">Initial Release</span></span>
