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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001500"
---
# <a name="release-notes"></a><span data-ttu-id="13798-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="13798-103">Release notes</span></span>

<span data-ttu-id="13798-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13798-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="13798-105">6.11.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-106">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-107">Corrigir o problema com Get-AzureRmSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="13798-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="13798-108">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="13798-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="13798-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="13798-109">AzureRM.Backup</span></span>
* <span data-ttu-id="13798-110">Cmdlets do Backup do Azure preteridos.</span><span class="sxs-lookup"><span data-stu-id="13798-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-111">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-112">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para 'New-AzureRmVm'</span><span class="sxs-lookup"><span data-stu-id="13798-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="13798-113">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="13798-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="13798-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="13798-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="13798-115">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="13798-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="13798-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: obtém ou lista regras de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="13798-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="13798-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: adiciona uma regra de rede virtual para a conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="13798-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="13798-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="13798-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="13798-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="13798-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-120">AzureRM.Network</span></span>
* <span data-ttu-id="13798-121">Atualize o cmdlet Test-AzureRmNetworkWatcherConnectivity, passe o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="13798-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="13798-122">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="13798-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-123">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-124">Corrija o problema onde Get-AzureRMRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="13798-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="13798-125">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="13798-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="13798-126">6.10.0 – outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="13798-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-127">Azure.Storage</span></span>
* <span data-ttu-id="13798-128">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="13798-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="13798-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="13798-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="13798-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="13798-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="13798-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="13798-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="13798-132">Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="13798-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-133">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-134">Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="13798-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="13798-135">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="13798-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="13798-136">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="13798-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="13798-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13798-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="13798-138">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="13798-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-139">AzureRM.Network</span></span>
* <span data-ttu-id="13798-140">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="13798-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="13798-141">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="13798-141">new cmdlets added</span></span>
    - <span data-ttu-id="13798-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="13798-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="13798-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="13798-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="13798-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="13798-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="13798-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="13798-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="13798-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="13798-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="13798-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="13798-148">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="13798-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="13798-149">Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="13798-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="13798-150">Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="13798-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="13798-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="13798-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="13798-152">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="13798-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="13798-153">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="13798-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-154">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-155">Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="13798-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="13798-156">Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="13798-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-157">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-158">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="13798-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="13798-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-159">AzureRM.Storage</span></span>
* <span data-ttu-id="13798-160">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="13798-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="13798-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="13798-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-162">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-163">Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="13798-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="13798-164">Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="13798-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="13798-165">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="13798-166">Geral</span><span class="sxs-lookup"><span data-stu-id="13798-166">General</span></span>
* <span data-ttu-id="13798-167">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="13798-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="13798-168">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-168">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-169">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="13798-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="13798-170">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="13798-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="13798-171">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13798-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="13798-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-172">Azure.Storage</span></span>
* <span data-ttu-id="13798-173">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="13798-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="13798-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="13798-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="13798-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="13798-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="13798-176">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="13798-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="13798-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-177">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-178">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="13798-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="13798-179">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="13798-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="13798-180">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="13798-181">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="13798-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="13798-182">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="13798-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="13798-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="13798-183">AzureRM.Dns</span></span>
* <span data-ttu-id="13798-184">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="13798-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="13798-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="13798-185">AzureRM.Insights</span></span>
* <span data-ttu-id="13798-186">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="13798-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="13798-187">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="13798-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="13798-188">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="13798-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="13798-189">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="13798-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="13798-190">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="13798-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-191">AzureRM.Network</span></span>
* <span data-ttu-id="13798-192">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13798-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="13798-193">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="13798-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="13798-194">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="13798-195">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="13798-196">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="13798-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="13798-197">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13798-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="13798-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="13798-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="13798-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="13798-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="13798-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="13798-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="13798-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="13798-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="13798-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="13798-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="13798-203">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13798-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="13798-204">Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="13798-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="13798-205">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="13798-206">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="13798-207">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="13798-208">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="13798-209">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="13798-210">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="13798-211">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="13798-212">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="13798-213">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="13798-214">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="13798-215">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="13798-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="13798-216">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="13798-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="13798-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="13798-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="13798-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="13798-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="13798-226">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="13798-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13798-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="13798-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13798-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="13798-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="13798-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="13798-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="13798-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="13798-231">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="13798-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13798-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="13798-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13798-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="13798-234">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="13798-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="13798-235">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="13798-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="13798-236">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="13798-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="13798-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="13798-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="13798-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="13798-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="13798-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="13798-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="13798-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="13798-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="13798-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="13798-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13798-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="13798-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13798-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="13798-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="13798-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="13798-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="13798-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="13798-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="13798-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="13798-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="13798-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="13798-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="13798-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="13798-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="13798-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="13798-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="13798-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="13798-256">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="13798-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="13798-257">New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="13798-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="13798-258">Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela</span><span class="sxs-lookup"><span data-stu-id="13798-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="13798-259">Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="13798-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="13798-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="13798-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="13798-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="13798-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="13798-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="13798-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="13798-263">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="13798-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="13798-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="13798-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="13798-265">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="13798-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-266">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-267">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="13798-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="13798-268">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="13798-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="13798-269">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="13798-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="13798-270">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="13798-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="13798-271">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="13798-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-273">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="13798-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="13798-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="13798-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="13798-275">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="13798-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="13798-276">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="13798-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="13798-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-277">AzureRM.Storage</span></span>
* <span data-ttu-id="13798-278">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="13798-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13798-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="13798-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="13798-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="13798-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="13798-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="13798-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="13798-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="13798-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="13798-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="13798-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="13798-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="13798-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="13798-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="13798-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="13798-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="13798-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="13798-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-290">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-291">Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="13798-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="13798-292">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="13798-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="13798-293">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="13798-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="13798-294">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="13798-295">Geral</span><span class="sxs-lookup"><span data-stu-id="13798-295">General</span></span>
* <span data-ttu-id="13798-296">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="13798-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="13798-297">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="13798-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="13798-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="13798-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="13798-299">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="13798-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="13798-300">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="13798-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="13798-301">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="13798-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="13798-302">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="13798-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="13798-303">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="13798-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="13798-304">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="13798-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="13798-305">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="13798-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="13798-306">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="13798-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="13798-307">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="13798-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="13798-308">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="13798-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="13798-309">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="13798-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="13798-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-310">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-311">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="13798-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="13798-312">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="13798-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="13798-313">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="13798-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="13798-314">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="13798-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-315">AzureRM.Network</span></span>
* <span data-ttu-id="13798-316">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="13798-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="13798-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="13798-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="13798-318">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="13798-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="13798-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-319">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-320">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="13798-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-322">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="13798-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="13798-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="13798-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="13798-324">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="13798-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="13798-325">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="13798-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="13798-326">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="13798-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="13798-327">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="13798-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="13798-328">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="13798-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="13798-329">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="13798-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="13798-330">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="13798-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="13798-331">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="13798-332">Geral</span><span class="sxs-lookup"><span data-stu-id="13798-332">General</span></span>
* <span data-ttu-id="13798-333">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="13798-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="13798-334">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-334">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-335">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="13798-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-336">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-337">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="13798-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="13798-338">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="13798-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="13798-339">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="13798-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="13798-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="13798-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="13798-341">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="13798-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-342">AzureRM.Network</span></span>
* <span data-ttu-id="13798-343">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="13798-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="13798-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="13798-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="13798-345">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="13798-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-346">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-347">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="13798-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-349">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="13798-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="13798-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="13798-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="13798-351">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="13798-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="13798-352">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="13798-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="13798-353">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="13798-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="13798-354">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="13798-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="13798-355">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="13798-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="13798-356">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="13798-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="13798-357">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="13798-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-358">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-359">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="13798-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="13798-360">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-361">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-361">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-362">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="13798-363">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="13798-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="13798-364">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="13798-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="13798-365">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="13798-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="13798-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-366">Azure.Storage</span></span>
* <span data-ttu-id="13798-367">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="13798-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="13798-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="13798-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="13798-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="13798-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="13798-370">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="13798-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="13798-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="13798-372">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="13798-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="13798-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="13798-374">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="13798-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="13798-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="13798-376">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="13798-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="13798-377">AzureRM.Automation</span></span>
* <span data-ttu-id="13798-378">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="13798-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="13798-379">AzureRM.Backup</span></span>
* <span data-ttu-id="13798-380">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="13798-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="13798-381">AzureRM.Batch</span></span>
* <span data-ttu-id="13798-382">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="13798-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="13798-383">AzureRM.Billing</span></span>
* <span data-ttu-id="13798-384">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="13798-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="13798-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="13798-386">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="13798-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="13798-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="13798-388">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-389">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-390">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="13798-391">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="13798-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="13798-392">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="13798-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="13798-393">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="13798-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="13798-394">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="13798-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="13798-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="13798-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="13798-396">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="13798-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="13798-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="13798-398">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="13798-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13798-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="13798-400">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="13798-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="13798-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="13798-402">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="13798-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13798-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="13798-404">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="13798-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="13798-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="13798-406">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="13798-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="13798-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="13798-408">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="13798-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="13798-409">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="13798-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="13798-410">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="13798-411">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="13798-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="13798-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="13798-413">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="13798-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="13798-414">AzureRM.Dns</span></span>
* <span data-ttu-id="13798-415">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="13798-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="13798-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="13798-417">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="13798-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="13798-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="13798-419">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="13798-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="13798-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="13798-421">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="13798-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="13798-422">AzureRM.Insights</span></span>
* <span data-ttu-id="13798-423">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="13798-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="13798-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="13798-425">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="13798-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-427">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="13798-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="13798-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="13798-429">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="13798-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="13798-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="13798-431">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="13798-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="13798-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="13798-433">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="13798-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="13798-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="13798-435">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="13798-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="13798-436">AzureRM.Media</span></span>
* <span data-ttu-id="13798-437">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-438">AzureRM.Network</span></span>
* <span data-ttu-id="13798-439">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13798-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="13798-440">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="13798-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="13798-441">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13798-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="13798-442">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="13798-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="13798-443">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="13798-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="13798-444">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="13798-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="13798-445">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="13798-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="13798-446">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="13798-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="13798-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="13798-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="13798-448">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="13798-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="13798-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="13798-450">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="13798-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="13798-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="13798-452">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="13798-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="13798-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="13798-454">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="13798-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="13798-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="13798-456">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="13798-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="13798-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="13798-458">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="13798-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="13798-459">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="13798-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="13798-460">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="13798-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="13798-461">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="13798-462">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="13798-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="13798-463">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="13798-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="13798-464">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="13798-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="13798-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="13798-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="13798-466">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="13798-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="13798-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="13798-468">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="13798-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="13798-469">AzureRM.Relay</span></span>
* <span data-ttu-id="13798-470">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-471">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-472">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="13798-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="13798-473">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="13798-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="13798-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="13798-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="13798-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="13798-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="13798-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="13798-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="13798-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="13798-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="13798-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="13798-481">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="13798-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="13798-482">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="13798-483">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="13798-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="13798-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="13798-485">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-487">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="13798-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="13798-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="13798-489">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-490">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-491">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="13798-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-492">AzureRM.Storage</span></span>
* <span data-ttu-id="13798-493">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="13798-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="13798-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="13798-495">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="13798-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="13798-496">AzureRM.Tags</span></span>
* <span data-ttu-id="13798-497">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="13798-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="13798-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="13798-499">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="13798-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="13798-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="13798-501">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-502">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-503">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="13798-504">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="13798-505">Geral</span><span class="sxs-lookup"><span data-stu-id="13798-505">General</span></span>
* <span data-ttu-id="13798-506">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="13798-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="13798-507">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-507">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-508">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="13798-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="13798-509">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="13798-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-510">Azure.Storage</span></span>
* <span data-ttu-id="13798-511">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13798-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="13798-512">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="13798-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="13798-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="13798-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="13798-514">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="13798-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="13798-515">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="13798-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="13798-516">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="13798-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="13798-517">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="13798-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="13798-518">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="13798-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="13798-519">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="13798-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-520">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-521">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="13798-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="13798-522">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="13798-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="13798-523">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="13798-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="13798-524">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="13798-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="13798-525">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="13798-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="13798-526">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="13798-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="13798-527">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="13798-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="13798-528">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="13798-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="13798-529">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="13798-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="13798-530">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="13798-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="13798-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13798-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="13798-532">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="13798-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="13798-533">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="13798-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="13798-534">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="13798-535">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="13798-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="13798-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="13798-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="13798-537">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="13798-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="13798-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="13798-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="13798-539">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="13798-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="13798-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="13798-540">AzureRM.Insights</span></span>
* <span data-ttu-id="13798-541">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="13798-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="13798-542">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="13798-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="13798-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-544">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-545">AzureRM.Network</span></span>
* <span data-ttu-id="13798-546">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="13798-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-547">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-548">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="13798-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="13798-549">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="13798-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-551">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="13798-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="13798-552">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="13798-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="13798-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-553">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-554">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="13798-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="13798-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="13798-556">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="13798-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="13798-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="13798-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="13798-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="13798-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="13798-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="13798-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="13798-560">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13798-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="13798-561">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="13798-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="13798-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-562">AzureRM.Storage</span></span>
* <span data-ttu-id="13798-563">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="13798-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="13798-564">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="13798-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="13798-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13798-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="13798-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13798-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="13798-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="13798-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="13798-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="13798-568">AzureRM.Tags</span></span>
* <span data-ttu-id="13798-569">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="13798-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="13798-570">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-571">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-571">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-572">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="13798-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="13798-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-573">Azure.Storage</span></span>
* <span data-ttu-id="13798-574">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="13798-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="13798-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="13798-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="13798-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="13798-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="13798-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="13798-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="13798-578">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="13798-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="13798-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="13798-579">AzureRM.Automation</span></span>
* <span data-ttu-id="13798-580">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="13798-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-581">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-582">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="13798-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="13798-583">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="13798-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="13798-584">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="13798-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="13798-585">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="13798-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="13798-586">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="13798-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="13798-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="13798-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="13798-588">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="13798-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="13798-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-590">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13798-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="13798-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="13798-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="13798-592">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="13798-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-593">AzureRM.Network</span></span>
* <span data-ttu-id="13798-594">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="13798-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="13798-595">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="13798-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="13798-596">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="13798-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="13798-597">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="13798-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="13798-598">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="13798-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="13798-599">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="13798-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="13798-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="13798-600">AzureRM.Relay</span></span>
* <span data-ttu-id="13798-601">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="13798-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-602">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-603">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="13798-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="13798-604">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="13798-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="13798-605">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="13798-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="13798-606">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="13798-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="13798-607">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="13798-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-609">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="13798-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="13798-610">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="13798-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="13798-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13798-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="13798-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13798-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="13798-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13798-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="13798-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13798-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="13798-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="13798-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="13798-616">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="13798-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="13798-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="13798-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="13798-618">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="13798-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-619">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-620">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="13798-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="13798-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="13798-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-623">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-624">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="13798-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="13798-625">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="13798-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="13798-626">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="13798-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="13798-627">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="13798-628">Geral</span><span class="sxs-lookup"><span data-stu-id="13798-628">General</span></span>
* <span data-ttu-id="13798-629">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="13798-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="13798-630">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-630">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-631">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="13798-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-632">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-633">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="13798-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="13798-634">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="13798-635">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="13798-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="13798-636">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="13798-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="13798-637">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="13798-638">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="13798-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="13798-639">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="13798-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="13798-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="13798-641">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="13798-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="13798-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="13798-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="13798-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="13798-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="13798-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="13798-646">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="13798-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="13798-647">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="13798-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="13798-648">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="13798-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="13798-649">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="13798-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="13798-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="13798-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="13798-651">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="13798-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="13798-652">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="13798-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="13798-653">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="13798-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="13798-654">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="13798-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="13798-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-656">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="13798-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-657">AzureRM.Network</span></span>
* <span data-ttu-id="13798-658">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="13798-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="13798-659">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="13798-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="13798-660">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="13798-661">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="13798-662">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="13798-663">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="13798-664">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="13798-665">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="13798-666">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="13798-667">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="13798-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="13798-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="13798-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="13798-669">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="13798-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="13798-670">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="13798-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="13798-671">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="13798-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-672">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-673">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="13798-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="13798-674">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="13798-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="13798-675">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="13798-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="13798-676">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="13798-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="13798-677">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="13798-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="13798-678">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="13798-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="13798-679">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="13798-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="13798-680">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="13798-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="13798-681">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="13798-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="13798-682">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="13798-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="13798-683">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="13798-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="13798-684">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="13798-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="13798-685">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="13798-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="13798-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="13798-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="13798-687">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="13798-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-688">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-689">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="13798-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="13798-690">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="13798-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="13798-691">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-692">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-692">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-693">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="13798-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="13798-694">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="13798-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="13798-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="13798-695">Azure.Storage</span></span>
* <span data-ttu-id="13798-696">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="13798-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-697">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-698">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="13798-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="13798-699">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="13798-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="13798-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="13798-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="13798-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="13798-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="13798-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="13798-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="13798-703">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="13798-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="13798-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13798-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="13798-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13798-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="13798-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13798-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="13798-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13798-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="13798-708">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="13798-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="13798-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="13798-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="13798-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="13798-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="13798-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="13798-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="13798-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="13798-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="13798-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="13798-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="13798-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="13798-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="13798-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="13798-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="13798-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="13798-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="13798-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="13798-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="13798-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="13798-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="13798-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="13798-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="13798-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="13798-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="13798-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="13798-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="13798-724">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="13798-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="13798-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-726">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="13798-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="13798-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="13798-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="13798-728">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="13798-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="13798-729">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="13798-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="13798-730">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="13798-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="13798-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="13798-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="13798-732">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="13798-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="13798-733">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="13798-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-734">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-735">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="13798-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="13798-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="13798-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="13798-737">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="13798-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-738">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-739">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="13798-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="13798-740">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="13798-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="13798-741">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="13798-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="13798-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="13798-743">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="13798-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="13798-744">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-745">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-745">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-746">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="13798-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="13798-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="13798-747">AzureRM.Compute</span></span>
* <span data-ttu-id="13798-748">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="13798-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="13798-749">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="13798-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="13798-750">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="13798-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="13798-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="13798-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="13798-752">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="13798-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="13798-753">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="13798-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="13798-754">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="13798-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="13798-755">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="13798-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="13798-756">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="13798-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="13798-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="13798-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="13798-758">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="13798-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="13798-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-759">AzureRM.Network</span></span>
* <span data-ttu-id="13798-760">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="13798-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="13798-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="13798-761">AzureRM.Resources</span></span>
* <span data-ttu-id="13798-762">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="13798-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="13798-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="13798-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="13798-764">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="13798-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="13798-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-765">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-766">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="13798-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="13798-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13798-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="13798-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="13798-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="13798-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="13798-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="13798-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="13798-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="13798-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13798-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="13798-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="13798-772">AzureRM.Websites</span></span>
* <span data-ttu-id="13798-773">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="13798-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="13798-774">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="13798-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="13798-775">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="13798-775">AzureRM.Profile</span></span>
* <span data-ttu-id="13798-776">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="13798-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="13798-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="13798-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="13798-778">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="13798-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="13798-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="13798-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="13798-780">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="13798-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="13798-781">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="13798-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="13798-782">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="13798-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="13798-783">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="13798-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="13798-784">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="13798-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="13798-785">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="13798-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="13798-786">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="13798-786">Added support for MSI identity</span></span>
* <span data-ttu-id="13798-787">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="13798-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="13798-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="13798-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="13798-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="13798-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="13798-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="13798-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="13798-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="13798-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="13798-792">AzureRM.Batch</span></span>
* <span data-ttu-id="13798-793">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="13798-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="13798-794">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="13798-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="13798-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="13798-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="13798-796">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="13798-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="13798-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="13798-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="13798-798">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="13798-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="13798-799">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="13798-800">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="13798-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="13798-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="13798-801">AzureRM.Network</span></span>
* <span data-ttu-id="13798-802">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="13798-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="13798-803">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="13798-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="13798-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="13798-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="13798-805">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="13798-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="13798-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="13798-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="13798-807">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="13798-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="13798-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="13798-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="13798-809">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="13798-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="13798-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="13798-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="13798-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="13798-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="13798-812">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="13798-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="13798-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="13798-813">AzureRM.Sql</span></span>
* <span data-ttu-id="13798-814">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="13798-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="13798-815">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="13798-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="13798-816">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="13798-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="13798-817">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="13798-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="13798-818">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="13798-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="13798-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13798-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="13798-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="13798-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="13798-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="13798-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="13798-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="13798-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="13798-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13798-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="13798-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="13798-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="13798-825">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="13798-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
