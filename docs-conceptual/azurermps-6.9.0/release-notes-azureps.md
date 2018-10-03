---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178996"
---
# <a name="release-notes"></a><span data-ttu-id="6c1bb-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="6c1bb-103">Release notes</span></span>

<span data-ttu-id="6c1bb-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="6c1bb-105">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c1bb-106">Geral</span><span class="sxs-lookup"><span data-stu-id="6c1bb-106">General</span></span>
* <span data-ttu-id="6c1bb-107">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-108">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-108">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-109">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="6c1bb-110">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="6c1bb-111">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c1bb-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="6c1bb-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-112">Azure.Storage</span></span>
* <span data-ttu-id="6c1bb-113">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="6c1bb-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c1bb-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6c1bb-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c1bb-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="6c1bb-116">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-117">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-118">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="6c1bb-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="6c1bb-119">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6c1bb-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="6c1bb-120">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6c1bb-121">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6c1bb-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="6c1bb-122">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6c1bb-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6c1bb-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6c1bb-123">AzureRM.Dns</span></span>
* <span data-ttu-id="6c1bb-124">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="6c1bb-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6c1bb-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-125">AzureRM.Insights</span></span>
* <span data-ttu-id="6c1bb-126">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="6c1bb-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="6c1bb-127">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="6c1bb-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="6c1bb-128">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="6c1bb-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="6c1bb-129">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="6c1bb-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="6c1bb-130">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="6c1bb-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-131">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-132">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="6c1bb-133">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="6c1bb-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="6c1bb-134">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="6c1bb-135">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="6c1bb-136">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="6c1bb-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="6c1bb-137">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="6c1bb-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6c1bb-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6c1bb-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6c1bb-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6c1bb-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="6c1bb-143">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6c1bb-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="6c1bb-144">Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="6c1bb-145">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="6c1bb-146">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="6c1bb-147">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="6c1bb-148">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="6c1bb-149">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="6c1bb-150">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="6c1bb-151">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="6c1bb-152">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="6c1bb-153">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="6c1bb-154">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="6c1bb-155">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="6c1bb-156">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="6c1bb-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6c1bb-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6c1bb-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6c1bb-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="6c1bb-166">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="6c1bb-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6c1bb-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6c1bb-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6c1bb-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="6c1bb-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6c1bb-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="6c1bb-171">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="6c1bb-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6c1bb-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="6c1bb-174">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c1bb-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="6c1bb-175">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="6c1bb-176">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="6c1bb-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6c1bb-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6c1bb-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6c1bb-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6c1bb-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="6c1bb-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6c1bb-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6c1bb-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6c1bb-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6c1bb-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6c1bb-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6c1bb-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="6c1bb-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="6c1bb-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="6c1bb-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="6c1bb-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6c1bb-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6c1bb-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6c1bb-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6c1bb-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="6c1bb-196">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="6c1bb-197">New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="6c1bb-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="6c1bb-198">Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela</span><span class="sxs-lookup"><span data-stu-id="6c1bb-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="6c1bb-199">Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="6c1bb-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="6c1bb-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="6c1bb-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="6c1bb-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="6c1bb-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6c1bb-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6c1bb-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6c1bb-203">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6c1bb-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c1bb-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6c1bb-205">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-206">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-207">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="6c1bb-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="6c1bb-208">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c1bb-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="6c1bb-209">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="6c1bb-210">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="6c1bb-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="6c1bb-211">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="6c1bb-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-213">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="6c1bb-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="6c1bb-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="6c1bb-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="6c1bb-215">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="6c1bb-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="6c1bb-216">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6c1bb-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-217">AzureRM.Storage</span></span>
* <span data-ttu-id="6c1bb-218">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="6c1bb-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6c1bb-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="6c1bb-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6c1bb-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6c1bb-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6c1bb-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6c1bb-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6c1bb-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="6c1bb-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="6c1bb-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="6c1bb-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="6c1bb-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6c1bb-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6c1bb-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6c1bb-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-230">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-231">Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6c1bb-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="6c1bb-232">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6c1bb-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="6c1bb-233">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6c1bb-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="6c1bb-234">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c1bb-235">Geral</span><span class="sxs-lookup"><span data-stu-id="6c1bb-235">General</span></span>
* <span data-ttu-id="6c1bb-236">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c1bb-237">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="6c1bb-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c1bb-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c1bb-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c1bb-239">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c1bb-240">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="6c1bb-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="6c1bb-241">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="6c1bb-242">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="6c1bb-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="6c1bb-243">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="6c1bb-244">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="6c1bb-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="6c1bb-245">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="6c1bb-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="6c1bb-246">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="6c1bb-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="6c1bb-247">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="6c1bb-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="6c1bb-248">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="6c1bb-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="6c1bb-249">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="6c1bb-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-250">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-251">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6c1bb-252">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6c1bb-253">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6c1bb-254">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="6c1bb-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-255">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-256">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6c1bb-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c1bb-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c1bb-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c1bb-258">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="6c1bb-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-259">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-260">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-262">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c1bb-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c1bb-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c1bb-264">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6c1bb-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6c1bb-265">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6c1bb-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6c1bb-266">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6c1bb-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6c1bb-267">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6c1bb-268">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="6c1bb-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6c1bb-269">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="6c1bb-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6c1bb-270">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="6c1bb-271">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c1bb-272">Geral</span><span class="sxs-lookup"><span data-stu-id="6c1bb-272">General</span></span>
* <span data-ttu-id="6c1bb-273">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-274">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-274">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-275">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="6c1bb-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-276">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-277">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6c1bb-278">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6c1bb-279">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="6c1bb-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6c1bb-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="6c1bb-281">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-282">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-283">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6c1bb-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c1bb-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c1bb-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c1bb-285">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="6c1bb-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-286">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-287">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-289">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="6c1bb-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c1bb-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c1bb-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c1bb-291">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6c1bb-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6c1bb-292">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6c1bb-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6c1bb-293">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6c1bb-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6c1bb-294">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6c1bb-295">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="6c1bb-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6c1bb-296">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="6c1bb-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6c1bb-297">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-298">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-299">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="6c1bb-300">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-301">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-301">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-302">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c1bb-303">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="6c1bb-304">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="6c1bb-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="6c1bb-305">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="6c1bb-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="6c1bb-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-306">Azure.Storage</span></span>
* <span data-ttu-id="6c1bb-307">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="6c1bb-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="6c1bb-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6c1bb-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c1bb-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c1bb-310">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="6c1bb-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="6c1bb-312">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c1bb-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c1bb-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c1bb-314">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="6c1bb-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="6c1bb-316">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6c1bb-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6c1bb-317">AzureRM.Automation</span></span>
* <span data-ttu-id="6c1bb-318">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="6c1bb-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="6c1bb-319">AzureRM.Backup</span></span>
* <span data-ttu-id="6c1bb-320">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6c1bb-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6c1bb-321">AzureRM.Batch</span></span>
* <span data-ttu-id="6c1bb-322">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="6c1bb-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="6c1bb-323">AzureRM.Billing</span></span>
* <span data-ttu-id="6c1bb-324">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6c1bb-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6c1bb-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="6c1bb-326">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="6c1bb-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="6c1bb-328">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-329">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-330">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c1bb-331">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="6c1bb-332">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="6c1bb-333">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6c1bb-334">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="6c1bb-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6c1bb-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6c1bb-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="6c1bb-336">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="6c1bb-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6c1bb-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="6c1bb-338">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="6c1bb-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="6c1bb-340">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="6c1bb-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6c1bb-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="6c1bb-342">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c1bb-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c1bb-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c1bb-344">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6c1bb-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c1bb-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6c1bb-346">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c1bb-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c1bb-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c1bb-348">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="6c1bb-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="6c1bb-349">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6c1bb-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6c1bb-350">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c1bb-351">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="6c1bb-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6c1bb-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="6c1bb-353">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6c1bb-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6c1bb-354">AzureRM.Dns</span></span>
* <span data-ttu-id="6c1bb-355">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6c1bb-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c1bb-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6c1bb-357">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c1bb-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c1bb-359">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="6c1bb-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6c1bb-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="6c1bb-361">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6c1bb-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-362">AzureRM.Insights</span></span>
* <span data-ttu-id="6c1bb-363">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6c1bb-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="6c1bb-365">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-367">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6c1bb-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c1bb-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6c1bb-369">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="6c1bb-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6c1bb-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="6c1bb-371">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="6c1bb-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="6c1bb-373">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="6c1bb-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6c1bb-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="6c1bb-375">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="6c1bb-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="6c1bb-376">AzureRM.Media</span></span>
* <span data-ttu-id="6c1bb-377">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-378">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-379">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="6c1bb-380">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c1bb-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c1bb-381">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c1bb-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="6c1bb-382">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6c1bb-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6c1bb-383">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6c1bb-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6c1bb-384">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6c1bb-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6c1bb-385">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="6c1bb-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="6c1bb-386">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="6c1bb-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="6c1bb-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6c1bb-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="6c1bb-388">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="6c1bb-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6c1bb-390">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6c1bb-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6c1bb-392">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6c1bb-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6c1bb-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6c1bb-394">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="6c1bb-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="6c1bb-396">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c1bb-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c1bb-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c1bb-398">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="6c1bb-399">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="6c1bb-400">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="6c1bb-401">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6c1bb-402">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="6c1bb-403">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6c1bb-404">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6c1bb-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6c1bb-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6c1bb-406">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6c1bb-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6c1bb-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6c1bb-408">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6c1bb-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6c1bb-409">AzureRM.Relay</span></span>
* <span data-ttu-id="6c1bb-410">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-411">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-412">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="6c1bb-413">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="6c1bb-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c1bb-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c1bb-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c1bb-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c1bb-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="6c1bb-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="6c1bb-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6c1bb-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="6c1bb-421">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6c1bb-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="6c1bb-422">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="6c1bb-423">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6c1bb-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6c1bb-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6c1bb-425">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-427">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c1bb-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c1bb-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c1bb-429">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-430">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-431">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6c1bb-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-432">AzureRM.Storage</span></span>
* <span data-ttu-id="6c1bb-433">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="6c1bb-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c1bb-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="6c1bb-435">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6c1bb-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6c1bb-436">AzureRM.Tags</span></span>
* <span data-ttu-id="6c1bb-437">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c1bb-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c1bb-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c1bb-439">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="6c1bb-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6c1bb-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="6c1bb-441">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-442">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-443">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="6c1bb-444">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c1bb-445">Geral</span><span class="sxs-lookup"><span data-stu-id="6c1bb-445">General</span></span>
* <span data-ttu-id="6c1bb-446">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-447">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-447">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-448">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="6c1bb-449">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c1bb-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-450">Azure.Storage</span></span>
* <span data-ttu-id="6c1bb-451">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="6c1bb-452">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c1bb-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c1bb-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c1bb-454">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6c1bb-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6c1bb-455">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="6c1bb-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6c1bb-456">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6c1bb-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6c1bb-457">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="6c1bb-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6c1bb-458">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6c1bb-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6c1bb-459">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="6c1bb-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-460">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-461">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6c1bb-462">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6c1bb-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6c1bb-463">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6c1bb-464">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="6c1bb-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6c1bb-465">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6c1bb-466">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6c1bb-467">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6c1bb-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6c1bb-468">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6c1bb-469">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6c1bb-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6c1bb-470">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c1bb-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c1bb-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c1bb-472">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6c1bb-473">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6c1bb-474">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6c1bb-475">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c1bb-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c1bb-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c1bb-477">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="6c1bb-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c1bb-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c1bb-479">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="6c1bb-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6c1bb-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-480">AzureRM.Insights</span></span>
* <span data-ttu-id="6c1bb-481">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6c1bb-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6c1bb-482">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="6c1bb-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-484">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-485">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-486">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-487">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-488">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6c1bb-489">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-491">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="6c1bb-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6c1bb-492">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-493">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-494">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6c1bb-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6c1bb-496">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6c1bb-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6c1bb-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6c1bb-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6c1bb-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6c1bb-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6c1bb-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6c1bb-500">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6c1bb-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6c1bb-501">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6c1bb-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6c1bb-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-502">AzureRM.Storage</span></span>
* <span data-ttu-id="6c1bb-503">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="6c1bb-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6c1bb-504">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6c1bb-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6c1bb-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c1bb-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6c1bb-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c1bb-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6c1bb-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c1bb-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6c1bb-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6c1bb-508">AzureRM.Tags</span></span>
* <span data-ttu-id="6c1bb-509">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="6c1bb-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6c1bb-510">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-511">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-511">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-512">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c1bb-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-513">Azure.Storage</span></span>
* <span data-ttu-id="6c1bb-514">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="6c1bb-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6c1bb-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6c1bb-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6c1bb-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c1bb-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c1bb-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c1bb-518">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6c1bb-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6c1bb-519">AzureRM.Automation</span></span>
* <span data-ttu-id="6c1bb-520">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-521">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-522">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c1bb-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6c1bb-523">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6c1bb-524">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6c1bb-525">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6c1bb-526">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c1bb-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c1bb-528">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-530">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6c1bb-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6c1bb-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6c1bb-532">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6c1bb-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-533">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-534">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6c1bb-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6c1bb-535">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6c1bb-536">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="6c1bb-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6c1bb-537">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6c1bb-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6c1bb-538">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6c1bb-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6c1bb-539">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="6c1bb-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6c1bb-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6c1bb-540">AzureRM.Relay</span></span>
* <span data-ttu-id="6c1bb-541">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-542">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-543">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6c1bb-544">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6c1bb-545">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6c1bb-546">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6c1bb-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6c1bb-547">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="6c1bb-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-549">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="6c1bb-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6c1bb-550">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6c1bb-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c1bb-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c1bb-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c1bb-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6c1bb-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6c1bb-556">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c1bb-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c1bb-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c1bb-558">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-559">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-560">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="6c1bb-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6c1bb-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6c1bb-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-563">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-564">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6c1bb-565">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="6c1bb-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6c1bb-566">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="6c1bb-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6c1bb-567">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6c1bb-568">Geral</span><span class="sxs-lookup"><span data-stu-id="6c1bb-568">General</span></span>
* <span data-ttu-id="6c1bb-569">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-570">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-570">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-571">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="6c1bb-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-572">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-573">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="6c1bb-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6c1bb-574">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6c1bb-575">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6c1bb-576">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="6c1bb-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6c1bb-577">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6c1bb-578">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6c1bb-579">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6c1bb-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6c1bb-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6c1bb-581">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6c1bb-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6c1bb-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6c1bb-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c1bb-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c1bb-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c1bb-586">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6c1bb-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6c1bb-587">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6c1bb-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6c1bb-588">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="6c1bb-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6c1bb-589">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="6c1bb-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6c1bb-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6c1bb-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="6c1bb-591">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6c1bb-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6c1bb-592">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6c1bb-593">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6c1bb-594">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-596">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="6c1bb-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-597">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-598">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6c1bb-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6c1bb-599">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6c1bb-600">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6c1bb-601">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6c1bb-602">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c1bb-603">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c1bb-604">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6c1bb-605">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6c1bb-606">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6c1bb-607">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="6c1bb-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c1bb-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c1bb-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c1bb-609">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6c1bb-610">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6c1bb-611">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-612">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-613">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6c1bb-614">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6c1bb-615">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6c1bb-616">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c1bb-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6c1bb-617">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6c1bb-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6c1bb-618">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6c1bb-619">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="6c1bb-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6c1bb-620">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6c1bb-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6c1bb-621">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6c1bb-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6c1bb-622">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="6c1bb-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6c1bb-623">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="6c1bb-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6c1bb-624">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="6c1bb-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6c1bb-625">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="6c1bb-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6c1bb-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6c1bb-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6c1bb-627">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-628">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-629">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6c1bb-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6c1bb-630">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="6c1bb-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6c1bb-631">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-632">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-632">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-633">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="6c1bb-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6c1bb-634">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="6c1bb-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6c1bb-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-635">Azure.Storage</span></span>
* <span data-ttu-id="6c1bb-636">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-637">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-638">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="6c1bb-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6c1bb-639">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="6c1bb-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6c1bb-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6c1bb-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6c1bb-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6c1bb-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6c1bb-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6c1bb-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6c1bb-643">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="6c1bb-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6c1bb-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6c1bb-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6c1bb-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6c1bb-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6c1bb-648">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6c1bb-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6c1bb-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6c1bb-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6c1bb-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6c1bb-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6c1bb-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6c1bb-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6c1bb-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6c1bb-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6c1bb-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6c1bb-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6c1bb-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6c1bb-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6c1bb-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6c1bb-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c1bb-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6c1bb-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6c1bb-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6c1bb-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6c1bb-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6c1bb-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6c1bb-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6c1bb-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c1bb-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6c1bb-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6c1bb-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6c1bb-664">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-666">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6c1bb-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6c1bb-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6c1bb-668">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="6c1bb-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6c1bb-669">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="6c1bb-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6c1bb-670">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6c1bb-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6c1bb-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6c1bb-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6c1bb-672">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6c1bb-673">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-674">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-675">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6c1bb-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c1bb-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c1bb-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c1bb-677">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-678">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-679">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6c1bb-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6c1bb-680">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="6c1bb-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6c1bb-681">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6c1bb-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6c1bb-683">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c1bb-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6c1bb-684">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-685">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-685">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-686">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6c1bb-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6c1bb-687">AzureRM.Compute</span></span>
* <span data-ttu-id="6c1bb-688">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="6c1bb-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6c1bb-689">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="6c1bb-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6c1bb-690">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6c1bb-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6c1bb-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6c1bb-692">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6c1bb-693">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="6c1bb-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6c1bb-694">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="6c1bb-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6c1bb-695">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="6c1bb-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6c1bb-696">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="6c1bb-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6c1bb-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6c1bb-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6c1bb-698">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-699">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-700">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="6c1bb-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6c1bb-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6c1bb-701">AzureRM.Resources</span></span>
* <span data-ttu-id="6c1bb-702">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6c1bb-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6c1bb-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6c1bb-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6c1bb-704">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="6c1bb-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6c1bb-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-705">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-706">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="6c1bb-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6c1bb-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c1bb-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6c1bb-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6c1bb-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6c1bb-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6c1bb-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c1bb-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6c1bb-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c1bb-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6c1bb-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6c1bb-712">AzureRM.Websites</span></span>
* <span data-ttu-id="6c1bb-713">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6c1bb-714">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="6c1bb-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6c1bb-715">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6c1bb-715">AzureRM.Profile</span></span>
* <span data-ttu-id="6c1bb-716">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="6c1bb-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6c1bb-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6c1bb-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6c1bb-718">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6c1bb-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c1bb-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6c1bb-720">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="6c1bb-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6c1bb-721">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c1bb-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6c1bb-722">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="6c1bb-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6c1bb-723">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="6c1bb-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6c1bb-724">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="6c1bb-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6c1bb-725">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6c1bb-726">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="6c1bb-726">Added support for MSI identity</span></span>
* <span data-ttu-id="6c1bb-727">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="6c1bb-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6c1bb-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6c1bb-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6c1bb-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6c1bb-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6c1bb-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6c1bb-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6c1bb-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6c1bb-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6c1bb-732">AzureRM.Batch</span></span>
* <span data-ttu-id="6c1bb-733">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6c1bb-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6c1bb-734">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6c1bb-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6c1bb-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6c1bb-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="6c1bb-736">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="6c1bb-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6c1bb-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6c1bb-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6c1bb-738">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6c1bb-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6c1bb-739">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6c1bb-740">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6c1bb-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6c1bb-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6c1bb-741">AzureRM.Network</span></span>
* <span data-ttu-id="6c1bb-742">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6c1bb-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6c1bb-743">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="6c1bb-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6c1bb-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c1bb-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6c1bb-745">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6c1bb-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6c1bb-747">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6c1bb-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6c1bb-749">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="6c1bb-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6c1bb-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c1bb-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6c1bb-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6c1bb-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6c1bb-752">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="6c1bb-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6c1bb-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6c1bb-753">AzureRM.Sql</span></span>
* <span data-ttu-id="6c1bb-754">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="6c1bb-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6c1bb-755">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6c1bb-756">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6c1bb-757">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6c1bb-758">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6c1bb-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6c1bb-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c1bb-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6c1bb-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6c1bb-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6c1bb-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6c1bb-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6c1bb-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c1bb-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6c1bb-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6c1bb-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6c1bb-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6c1bb-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6c1bb-765">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="6c1bb-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
