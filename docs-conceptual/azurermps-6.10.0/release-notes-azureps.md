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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882047"
---
# <a name="release-notes"></a><span data-ttu-id="415cc-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="415cc-103">Release notes</span></span>

<span data-ttu-id="415cc-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="415cc-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="415cc-105">6.10.0 – outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="415cc-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-106">Azure.Storage</span></span>
* <span data-ttu-id="415cc-107">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="415cc-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="415cc-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="415cc-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="415cc-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="415cc-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="415cc-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="415cc-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="415cc-111">Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="415cc-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-112">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-113">Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="415cc-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="415cc-114">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="415cc-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="415cc-115">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="415cc-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="415cc-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="415cc-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="415cc-117">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="415cc-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-118">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-119">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="415cc-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="415cc-120">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="415cc-120">new cmdlets added</span></span>
    - <span data-ttu-id="415cc-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="415cc-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="415cc-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="415cc-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="415cc-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="415cc-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="415cc-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="415cc-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="415cc-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="415cc-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="415cc-127">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="415cc-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="415cc-128">Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="415cc-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="415cc-129">Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="415cc-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="415cc-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="415cc-131">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="415cc-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="415cc-132">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="415cc-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-133">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-134">Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="415cc-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="415cc-135">Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="415cc-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-136">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-137">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="415cc-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="415cc-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-138">AzureRM.Storage</span></span>
* <span data-ttu-id="415cc-139">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="415cc-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="415cc-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="415cc-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-141">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-142">Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="415cc-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="415cc-143">Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="415cc-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="415cc-144">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="415cc-145">Geral</span><span class="sxs-lookup"><span data-stu-id="415cc-145">General</span></span>
* <span data-ttu-id="415cc-146">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="415cc-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="415cc-147">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-147">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-148">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="415cc-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="415cc-149">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="415cc-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="415cc-150">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="415cc-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="415cc-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-151">Azure.Storage</span></span>
* <span data-ttu-id="415cc-152">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="415cc-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="415cc-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="415cc-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="415cc-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="415cc-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="415cc-155">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="415cc-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-156">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-157">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="415cc-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="415cc-158">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="415cc-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="415cc-159">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="415cc-160">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="415cc-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="415cc-161">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="415cc-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="415cc-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="415cc-162">AzureRM.Dns</span></span>
* <span data-ttu-id="415cc-163">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="415cc-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="415cc-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="415cc-164">AzureRM.Insights</span></span>
* <span data-ttu-id="415cc-165">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="415cc-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="415cc-166">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="415cc-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="415cc-167">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="415cc-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="415cc-168">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="415cc-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="415cc-169">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="415cc-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-170">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-171">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="415cc-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="415cc-172">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="415cc-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="415cc-173">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="415cc-174">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="415cc-175">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="415cc-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="415cc-176">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="415cc-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="415cc-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="415cc-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="415cc-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="415cc-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="415cc-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="415cc-182">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="415cc-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="415cc-183">Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="415cc-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="415cc-184">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="415cc-185">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="415cc-186">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="415cc-187">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="415cc-188">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="415cc-189">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="415cc-190">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="415cc-191">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="415cc-192">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="415cc-193">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="415cc-194">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="415cc-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="415cc-195">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="415cc-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="415cc-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="415cc-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="415cc-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="415cc-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="415cc-205">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="415cc-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="415cc-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="415cc-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="415cc-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="415cc-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="415cc-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="415cc-210">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="415cc-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="415cc-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="415cc-213">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="415cc-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="415cc-214">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="415cc-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="415cc-215">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="415cc-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="415cc-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="415cc-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="415cc-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="415cc-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="415cc-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="415cc-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="415cc-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="415cc-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="415cc-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="415cc-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="415cc-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="415cc-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="415cc-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="415cc-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="415cc-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="415cc-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="415cc-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="415cc-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="415cc-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="415cc-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="415cc-235">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="415cc-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="415cc-236">New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="415cc-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="415cc-237">Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela</span><span class="sxs-lookup"><span data-stu-id="415cc-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="415cc-238">Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="415cc-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="415cc-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="415cc-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="415cc-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="415cc-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="415cc-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="415cc-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="415cc-242">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="415cc-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="415cc-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="415cc-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="415cc-244">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="415cc-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-245">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-246">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="415cc-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="415cc-247">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="415cc-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="415cc-248">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="415cc-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="415cc-249">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="415cc-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="415cc-250">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="415cc-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-252">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="415cc-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="415cc-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="415cc-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="415cc-254">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="415cc-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="415cc-255">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="415cc-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="415cc-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-256">AzureRM.Storage</span></span>
* <span data-ttu-id="415cc-257">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="415cc-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="415cc-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="415cc-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="415cc-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="415cc-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="415cc-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="415cc-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="415cc-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="415cc-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="415cc-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="415cc-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="415cc-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="415cc-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="415cc-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="415cc-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="415cc-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="415cc-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="415cc-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-269">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-270">Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="415cc-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="415cc-271">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="415cc-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="415cc-272">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="415cc-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="415cc-273">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="415cc-274">Geral</span><span class="sxs-lookup"><span data-stu-id="415cc-274">General</span></span>
* <span data-ttu-id="415cc-275">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="415cc-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="415cc-276">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="415cc-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="415cc-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="415cc-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="415cc-278">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="415cc-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="415cc-279">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="415cc-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="415cc-280">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="415cc-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="415cc-281">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="415cc-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="415cc-282">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="415cc-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="415cc-283">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="415cc-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="415cc-284">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="415cc-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="415cc-285">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="415cc-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="415cc-286">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="415cc-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="415cc-287">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="415cc-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="415cc-288">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="415cc-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="415cc-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-289">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-290">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="415cc-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="415cc-291">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="415cc-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="415cc-292">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="415cc-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="415cc-293">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="415cc-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-294">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-295">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="415cc-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="415cc-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="415cc-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="415cc-297">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="415cc-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="415cc-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-298">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-299">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="415cc-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-301">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="415cc-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="415cc-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="415cc-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="415cc-303">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="415cc-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="415cc-304">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="415cc-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="415cc-305">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="415cc-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="415cc-306">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="415cc-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="415cc-307">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="415cc-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="415cc-308">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="415cc-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="415cc-309">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="415cc-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="415cc-310">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="415cc-311">Geral</span><span class="sxs-lookup"><span data-stu-id="415cc-311">General</span></span>
* <span data-ttu-id="415cc-312">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="415cc-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="415cc-313">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-313">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-314">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="415cc-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-315">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-316">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="415cc-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="415cc-317">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="415cc-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="415cc-318">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="415cc-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="415cc-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="415cc-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="415cc-320">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="415cc-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-321">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-322">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="415cc-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="415cc-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="415cc-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="415cc-324">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="415cc-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-325">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-326">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="415cc-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-328">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="415cc-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="415cc-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="415cc-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="415cc-330">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="415cc-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="415cc-331">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="415cc-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="415cc-332">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="415cc-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="415cc-333">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="415cc-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="415cc-334">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="415cc-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="415cc-335">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="415cc-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="415cc-336">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="415cc-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-337">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-338">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="415cc-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="415cc-339">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="415cc-340">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-340">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-341">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="415cc-342">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="415cc-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="415cc-343">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="415cc-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="415cc-344">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="415cc-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="415cc-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-345">Azure.Storage</span></span>
* <span data-ttu-id="415cc-346">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="415cc-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="415cc-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="415cc-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="415cc-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="415cc-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="415cc-349">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="415cc-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="415cc-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="415cc-351">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="415cc-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="415cc-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="415cc-353">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="415cc-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="415cc-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="415cc-355">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="415cc-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="415cc-356">AzureRM.Automation</span></span>
* <span data-ttu-id="415cc-357">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="415cc-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="415cc-358">AzureRM.Backup</span></span>
* <span data-ttu-id="415cc-359">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="415cc-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="415cc-360">AzureRM.Batch</span></span>
* <span data-ttu-id="415cc-361">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="415cc-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="415cc-362">AzureRM.Billing</span></span>
* <span data-ttu-id="415cc-363">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="415cc-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="415cc-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="415cc-365">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="415cc-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="415cc-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="415cc-367">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-368">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-369">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="415cc-370">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="415cc-371">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="415cc-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="415cc-372">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="415cc-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="415cc-373">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="415cc-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="415cc-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="415cc-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="415cc-375">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="415cc-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="415cc-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="415cc-377">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="415cc-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="415cc-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="415cc-379">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="415cc-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="415cc-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="415cc-381">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="415cc-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="415cc-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="415cc-383">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="415cc-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="415cc-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="415cc-385">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="415cc-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="415cc-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="415cc-387">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="415cc-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="415cc-388">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="415cc-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="415cc-389">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="415cc-390">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="415cc-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="415cc-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="415cc-392">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="415cc-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="415cc-393">AzureRM.Dns</span></span>
* <span data-ttu-id="415cc-394">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="415cc-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="415cc-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="415cc-396">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="415cc-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="415cc-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="415cc-398">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="415cc-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="415cc-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="415cc-400">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="415cc-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="415cc-401">AzureRM.Insights</span></span>
* <span data-ttu-id="415cc-402">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="415cc-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="415cc-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="415cc-404">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-406">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="415cc-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="415cc-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="415cc-408">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="415cc-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="415cc-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="415cc-410">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="415cc-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="415cc-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="415cc-412">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="415cc-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="415cc-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="415cc-414">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="415cc-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="415cc-415">AzureRM.Media</span></span>
* <span data-ttu-id="415cc-416">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-417">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-418">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="415cc-419">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="415cc-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="415cc-420">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="415cc-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="415cc-421">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="415cc-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="415cc-422">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="415cc-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="415cc-423">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="415cc-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="415cc-424">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="415cc-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="415cc-425">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="415cc-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="415cc-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="415cc-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="415cc-427">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="415cc-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="415cc-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="415cc-429">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="415cc-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="415cc-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="415cc-431">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="415cc-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="415cc-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="415cc-433">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="415cc-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="415cc-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="415cc-435">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="415cc-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="415cc-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="415cc-437">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="415cc-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="415cc-438">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="415cc-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="415cc-439">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="415cc-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="415cc-440">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="415cc-441">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="415cc-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="415cc-442">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="415cc-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="415cc-443">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="415cc-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="415cc-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="415cc-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="415cc-445">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="415cc-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="415cc-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="415cc-447">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="415cc-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="415cc-448">AzureRM.Relay</span></span>
* <span data-ttu-id="415cc-449">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-450">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-451">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="415cc-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="415cc-452">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="415cc-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="415cc-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="415cc-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="415cc-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="415cc-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="415cc-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="415cc-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="415cc-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="415cc-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="415cc-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="415cc-460">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="415cc-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="415cc-461">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="415cc-462">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="415cc-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="415cc-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="415cc-464">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-466">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="415cc-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="415cc-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="415cc-468">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-469">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-470">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="415cc-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-471">AzureRM.Storage</span></span>
* <span data-ttu-id="415cc-472">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="415cc-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="415cc-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="415cc-474">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="415cc-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="415cc-475">AzureRM.Tags</span></span>
* <span data-ttu-id="415cc-476">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="415cc-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="415cc-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="415cc-478">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="415cc-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="415cc-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="415cc-480">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-481">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-482">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="415cc-483">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="415cc-484">Geral</span><span class="sxs-lookup"><span data-stu-id="415cc-484">General</span></span>
* <span data-ttu-id="415cc-485">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="415cc-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="415cc-486">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-486">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-487">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="415cc-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="415cc-488">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="415cc-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-489">Azure.Storage</span></span>
* <span data-ttu-id="415cc-490">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415cc-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="415cc-491">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="415cc-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="415cc-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="415cc-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="415cc-493">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="415cc-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="415cc-494">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="415cc-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="415cc-495">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="415cc-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="415cc-496">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="415cc-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="415cc-497">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="415cc-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="415cc-498">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="415cc-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-499">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-500">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="415cc-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="415cc-501">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="415cc-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="415cc-502">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="415cc-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="415cc-503">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="415cc-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="415cc-504">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="415cc-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="415cc-505">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="415cc-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="415cc-506">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="415cc-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="415cc-507">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="415cc-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="415cc-508">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="415cc-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="415cc-509">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="415cc-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="415cc-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="415cc-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="415cc-511">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="415cc-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="415cc-512">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="415cc-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="415cc-513">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="415cc-514">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="415cc-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="415cc-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="415cc-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="415cc-516">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="415cc-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="415cc-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="415cc-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="415cc-518">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="415cc-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="415cc-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="415cc-519">AzureRM.Insights</span></span>
* <span data-ttu-id="415cc-520">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="415cc-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="415cc-521">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="415cc-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-523">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-524">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-525">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="415cc-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-526">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-527">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="415cc-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="415cc-528">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="415cc-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-530">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="415cc-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="415cc-531">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="415cc-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="415cc-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-532">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-533">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="415cc-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="415cc-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="415cc-535">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="415cc-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="415cc-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="415cc-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="415cc-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="415cc-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="415cc-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="415cc-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="415cc-539">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="415cc-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="415cc-540">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="415cc-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="415cc-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-541">AzureRM.Storage</span></span>
* <span data-ttu-id="415cc-542">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="415cc-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="415cc-543">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="415cc-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="415cc-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="415cc-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="415cc-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="415cc-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="415cc-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="415cc-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="415cc-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="415cc-547">AzureRM.Tags</span></span>
* <span data-ttu-id="415cc-548">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="415cc-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="415cc-549">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="415cc-550">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-550">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-551">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="415cc-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="415cc-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-552">Azure.Storage</span></span>
* <span data-ttu-id="415cc-553">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="415cc-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="415cc-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="415cc-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="415cc-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="415cc-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="415cc-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="415cc-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="415cc-557">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="415cc-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="415cc-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="415cc-558">AzureRM.Automation</span></span>
* <span data-ttu-id="415cc-559">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="415cc-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-560">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-561">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="415cc-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="415cc-562">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="415cc-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="415cc-563">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="415cc-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="415cc-564">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="415cc-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="415cc-565">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="415cc-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="415cc-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="415cc-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="415cc-567">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="415cc-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-569">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="415cc-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="415cc-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="415cc-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="415cc-571">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="415cc-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-572">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-573">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="415cc-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="415cc-574">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="415cc-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="415cc-575">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="415cc-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="415cc-576">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="415cc-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="415cc-577">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="415cc-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="415cc-578">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="415cc-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="415cc-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="415cc-579">AzureRM.Relay</span></span>
* <span data-ttu-id="415cc-580">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="415cc-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-581">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-582">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="415cc-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="415cc-583">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="415cc-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="415cc-584">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="415cc-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="415cc-585">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="415cc-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="415cc-586">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="415cc-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-588">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="415cc-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="415cc-589">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="415cc-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="415cc-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="415cc-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="415cc-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="415cc-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="415cc-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="415cc-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="415cc-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="415cc-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="415cc-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="415cc-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="415cc-595">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="415cc-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="415cc-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="415cc-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="415cc-597">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="415cc-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-598">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-599">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="415cc-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="415cc-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="415cc-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-602">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-603">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="415cc-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="415cc-604">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="415cc-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="415cc-605">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="415cc-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="415cc-606">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="415cc-607">Geral</span><span class="sxs-lookup"><span data-stu-id="415cc-607">General</span></span>
* <span data-ttu-id="415cc-608">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="415cc-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="415cc-609">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-609">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-610">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="415cc-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-611">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-612">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="415cc-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="415cc-613">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="415cc-614">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="415cc-615">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="415cc-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="415cc-616">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="415cc-617">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="415cc-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="415cc-618">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="415cc-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="415cc-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="415cc-620">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="415cc-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="415cc-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="415cc-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="415cc-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="415cc-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="415cc-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="415cc-625">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="415cc-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="415cc-626">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="415cc-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="415cc-627">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="415cc-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="415cc-628">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="415cc-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="415cc-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="415cc-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="415cc-630">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="415cc-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="415cc-631">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="415cc-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="415cc-632">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="415cc-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="415cc-633">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="415cc-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-635">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="415cc-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-636">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-637">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="415cc-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="415cc-638">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="415cc-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="415cc-639">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="415cc-640">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="415cc-641">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="415cc-642">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="415cc-643">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="415cc-644">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="415cc-645">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="415cc-646">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="415cc-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="415cc-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="415cc-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="415cc-648">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="415cc-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="415cc-649">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="415cc-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="415cc-650">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="415cc-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-651">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-652">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="415cc-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="415cc-653">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="415cc-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="415cc-654">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="415cc-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="415cc-655">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="415cc-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="415cc-656">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="415cc-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="415cc-657">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="415cc-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="415cc-658">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="415cc-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="415cc-659">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="415cc-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="415cc-660">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="415cc-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="415cc-661">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="415cc-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="415cc-662">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="415cc-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="415cc-663">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="415cc-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="415cc-664">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="415cc-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="415cc-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="415cc-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="415cc-666">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="415cc-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-667">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-668">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="415cc-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="415cc-669">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="415cc-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="415cc-670">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="415cc-671">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-671">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-672">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="415cc-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="415cc-673">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="415cc-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="415cc-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="415cc-674">Azure.Storage</span></span>
* <span data-ttu-id="415cc-675">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="415cc-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-676">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-677">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="415cc-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="415cc-678">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="415cc-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="415cc-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="415cc-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="415cc-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="415cc-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="415cc-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="415cc-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="415cc-682">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="415cc-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="415cc-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="415cc-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="415cc-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="415cc-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="415cc-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="415cc-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="415cc-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="415cc-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="415cc-687">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="415cc-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="415cc-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="415cc-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="415cc-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="415cc-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="415cc-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="415cc-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="415cc-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="415cc-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="415cc-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="415cc-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="415cc-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="415cc-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="415cc-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="415cc-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="415cc-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="415cc-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="415cc-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="415cc-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="415cc-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="415cc-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="415cc-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="415cc-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="415cc-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="415cc-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="415cc-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="415cc-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="415cc-703">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="415cc-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-705">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="415cc-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="415cc-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="415cc-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="415cc-707">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="415cc-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="415cc-708">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="415cc-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="415cc-709">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="415cc-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="415cc-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="415cc-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="415cc-711">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="415cc-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="415cc-712">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="415cc-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-713">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-714">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="415cc-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="415cc-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="415cc-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="415cc-716">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-717">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-718">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="415cc-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="415cc-719">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="415cc-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="415cc-720">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="415cc-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="415cc-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="415cc-722">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="415cc-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="415cc-723">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="415cc-724">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-724">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-725">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="415cc-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="415cc-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="415cc-726">AzureRM.Compute</span></span>
* <span data-ttu-id="415cc-727">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="415cc-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="415cc-728">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="415cc-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="415cc-729">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="415cc-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="415cc-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="415cc-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="415cc-731">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="415cc-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="415cc-732">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="415cc-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="415cc-733">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="415cc-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="415cc-734">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="415cc-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="415cc-735">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="415cc-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="415cc-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="415cc-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="415cc-737">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="415cc-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="415cc-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-738">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-739">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="415cc-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="415cc-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="415cc-740">AzureRM.Resources</span></span>
* <span data-ttu-id="415cc-741">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="415cc-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="415cc-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="415cc-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="415cc-743">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="415cc-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="415cc-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-744">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-745">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="415cc-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="415cc-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="415cc-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="415cc-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="415cc-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="415cc-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="415cc-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="415cc-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="415cc-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="415cc-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="415cc-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="415cc-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="415cc-751">AzureRM.Websites</span></span>
* <span data-ttu-id="415cc-752">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="415cc-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="415cc-753">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="415cc-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="415cc-754">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="415cc-754">AzureRM.Profile</span></span>
* <span data-ttu-id="415cc-755">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="415cc-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="415cc-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="415cc-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="415cc-757">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="415cc-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="415cc-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="415cc-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="415cc-759">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="415cc-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="415cc-760">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="415cc-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="415cc-761">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="415cc-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="415cc-762">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="415cc-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="415cc-763">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="415cc-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="415cc-764">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="415cc-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="415cc-765">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="415cc-765">Added support for MSI identity</span></span>
* <span data-ttu-id="415cc-766">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="415cc-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="415cc-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="415cc-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="415cc-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="415cc-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="415cc-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="415cc-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="415cc-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="415cc-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="415cc-771">AzureRM.Batch</span></span>
* <span data-ttu-id="415cc-772">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="415cc-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="415cc-773">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="415cc-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="415cc-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="415cc-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="415cc-775">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="415cc-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="415cc-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="415cc-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="415cc-777">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="415cc-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="415cc-778">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="415cc-779">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="415cc-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="415cc-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="415cc-780">AzureRM.Network</span></span>
* <span data-ttu-id="415cc-781">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="415cc-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="415cc-782">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="415cc-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="415cc-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="415cc-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="415cc-784">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="415cc-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="415cc-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="415cc-786">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="415cc-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="415cc-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="415cc-788">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="415cc-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="415cc-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="415cc-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="415cc-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="415cc-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="415cc-791">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="415cc-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="415cc-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="415cc-792">AzureRM.Sql</span></span>
* <span data-ttu-id="415cc-793">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="415cc-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="415cc-794">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="415cc-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="415cc-795">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="415cc-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="415cc-796">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="415cc-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="415cc-797">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="415cc-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="415cc-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="415cc-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="415cc-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="415cc-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="415cc-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="415cc-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="415cc-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="415cc-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="415cc-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="415cc-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="415cc-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="415cc-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="415cc-804">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="415cc-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
