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
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738097"
---
# <a name="release-notes"></a><span data-ttu-id="6dddb-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="6dddb-103">Release notes</span></span>

<span data-ttu-id="6dddb-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6dddb-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="6dddb-105">6.11.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-106">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-107">Corrigir o problema com Get-AzureRmSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="6dddb-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="6dddb-108">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6dddb-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="6dddb-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="6dddb-109">AzureRM.Backup</span></span>
* <span data-ttu-id="6dddb-110">Cmdlets do Backup do Azure preteridos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-111">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-112">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para 'New-AzureRmVm'</span><span class="sxs-lookup"><span data-stu-id="6dddb-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="6dddb-113">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6dddb-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6dddb-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6dddb-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6dddb-115">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="6dddb-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6dddb-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: obtém ou lista regras de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6dddb-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6dddb-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: adiciona uma regra de rede virtual para a conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6dddb-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6dddb-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="6dddb-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6dddb-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6dddb-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-120">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-121">Atualize o cmdlet Test-AzureRmNetworkWatcherConnectivity, passe o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="6dddb-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6dddb-122">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6dddb-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-123">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-124">Corrija o problema onde Get-AzureRMRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="6dddb-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6dddb-125">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="6dddb-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="6dddb-126">6.10.0 – outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6dddb-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-127">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-128">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="6dddb-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6dddb-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6dddb-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6dddb-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6dddb-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="6dddb-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="6dddb-132">Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="6dddb-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-133">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-134">Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="6dddb-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6dddb-135">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="6dddb-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="6dddb-136">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="6dddb-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6dddb-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6dddb-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6dddb-138">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6dddb-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-139">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-140">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6dddb-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6dddb-141">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="6dddb-141">new cmdlets added</span></span>
    - <span data-ttu-id="6dddb-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dddb-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="6dddb-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dddb-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="6dddb-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dddb-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="6dddb-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6dddb-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="6dddb-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="6dddb-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6dddb-148">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6dddb-149">Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6dddb-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="6dddb-150">Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6dddb-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6dddb-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6dddb-152">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="6dddb-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6dddb-153">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="6dddb-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-154">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-155">Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dddb-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="6dddb-156">Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="6dddb-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-157">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-158">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="6dddb-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6dddb-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-159">AzureRM.Storage</span></span>
* <span data-ttu-id="6dddb-160">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6dddb-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6dddb-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6dddb-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-162">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-163">Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="6dddb-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6dddb-164">Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6dddb-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="6dddb-165">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6dddb-166">Geral</span><span class="sxs-lookup"><span data-stu-id="6dddb-166">General</span></span>
* <span data-ttu-id="6dddb-167">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="6dddb-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-168">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-168">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-169">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="6dddb-170">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="6dddb-171">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dddb-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="6dddb-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-172">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-173">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="6dddb-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="6dddb-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6dddb-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6dddb-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6dddb-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="6dddb-176">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="6dddb-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-177">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-178">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="6dddb-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="6dddb-179">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6dddb-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="6dddb-180">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6dddb-181">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6dddb-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="6dddb-182">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6dddb-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6dddb-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6dddb-183">AzureRM.Dns</span></span>
* <span data-ttu-id="6dddb-184">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="6dddb-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6dddb-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6dddb-185">AzureRM.Insights</span></span>
* <span data-ttu-id="6dddb-186">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="6dddb-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="6dddb-187">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="6dddb-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="6dddb-188">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="6dddb-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="6dddb-189">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="6dddb-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="6dddb-190">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="6dddb-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-191">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-192">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6dddb-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="6dddb-193">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="6dddb-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="6dddb-194">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="6dddb-195">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="6dddb-196">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="6dddb-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="6dddb-197">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6dddb-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="6dddb-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6dddb-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6dddb-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6dddb-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="6dddb-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="6dddb-203">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6dddb-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="6dddb-204">Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="6dddb-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="6dddb-205">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="6dddb-206">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="6dddb-207">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="6dddb-208">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="6dddb-209">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="6dddb-210">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="6dddb-211">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="6dddb-212">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="6dddb-213">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="6dddb-214">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="6dddb-215">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6dddb-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="6dddb-216">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="6dddb-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="6dddb-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6dddb-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6dddb-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="6dddb-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="6dddb-226">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="6dddb-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6dddb-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6dddb-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6dddb-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="6dddb-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6dddb-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="6dddb-231">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="6dddb-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="6dddb-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="6dddb-234">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6dddb-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="6dddb-235">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6dddb-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="6dddb-236">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="6dddb-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="6dddb-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6dddb-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6dddb-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6dddb-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="6dddb-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="6dddb-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6dddb-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6dddb-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="6dddb-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6dddb-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6dddb-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="6dddb-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="6dddb-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="6dddb-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="6dddb-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="6dddb-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6dddb-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6dddb-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="6dddb-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6dddb-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="6dddb-256">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="6dddb-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="6dddb-257">New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="6dddb-258">Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela</span><span class="sxs-lookup"><span data-stu-id="6dddb-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="6dddb-259">Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="6dddb-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="6dddb-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="6dddb-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="6dddb-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6dddb-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6dddb-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6dddb-263">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6dddb-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6dddb-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6dddb-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6dddb-265">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="6dddb-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-266">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-267">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="6dddb-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="6dddb-268">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dddb-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="6dddb-269">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="6dddb-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="6dddb-270">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="6dddb-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="6dddb-271">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="6dddb-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-273">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="6dddb-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="6dddb-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="6dddb-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="6dddb-275">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="6dddb-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="6dddb-276">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="6dddb-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6dddb-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-277">AzureRM.Storage</span></span>
* <span data-ttu-id="6dddb-278">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="6dddb-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6dddb-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="6dddb-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6dddb-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6dddb-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6dddb-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6dddb-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6dddb-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6dddb-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6dddb-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="6dddb-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="6dddb-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="6dddb-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="6dddb-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="6dddb-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6dddb-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6dddb-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="6dddb-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-290">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-291">Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6dddb-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="6dddb-292">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6dddb-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="6dddb-293">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="6dddb-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="6dddb-294">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6dddb-295">Geral</span><span class="sxs-lookup"><span data-stu-id="6dddb-295">General</span></span>
* <span data-ttu-id="6dddb-296">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6dddb-297">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="6dddb-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6dddb-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6dddb-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6dddb-299">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6dddb-300">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="6dddb-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="6dddb-301">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="6dddb-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="6dddb-302">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="6dddb-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="6dddb-303">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="6dddb-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="6dddb-304">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="6dddb-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="6dddb-305">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="6dddb-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="6dddb-306">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="6dddb-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="6dddb-307">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="6dddb-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="6dddb-308">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="6dddb-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="6dddb-309">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="6dddb-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-310">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-311">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="6dddb-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6dddb-312">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6dddb-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6dddb-313">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="6dddb-314">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="6dddb-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-315">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-316">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6dddb-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6dddb-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6dddb-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6dddb-318">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="6dddb-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="6dddb-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-319">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-320">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6dddb-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-322">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="6dddb-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6dddb-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6dddb-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6dddb-324">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6dddb-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6dddb-325">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6dddb-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6dddb-326">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6dddb-327">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6dddb-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6dddb-328">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="6dddb-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6dddb-329">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="6dddb-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6dddb-330">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6dddb-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="6dddb-331">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6dddb-332">Geral</span><span class="sxs-lookup"><span data-stu-id="6dddb-332">General</span></span>
* <span data-ttu-id="6dddb-333">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-334">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-334">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-335">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="6dddb-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-336">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-337">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="6dddb-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="6dddb-338">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="6dddb-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="6dddb-339">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="6dddb-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6dddb-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="6dddb-341">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="6dddb-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-342">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-343">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6dddb-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6dddb-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6dddb-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6dddb-345">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="6dddb-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-346">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-347">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="6dddb-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-349">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="6dddb-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6dddb-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6dddb-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6dddb-351">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6dddb-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="6dddb-352">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="6dddb-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="6dddb-353">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="6dddb-354">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6dddb-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="6dddb-355">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="6dddb-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="6dddb-356">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="6dddb-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="6dddb-357">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="6dddb-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-358">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-359">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="6dddb-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="6dddb-360">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-361">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-361">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-362">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6dddb-363">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="6dddb-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="6dddb-364">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="6dddb-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="6dddb-365">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="6dddb-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="6dddb-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-366">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-367">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="6dddb-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="6dddb-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6dddb-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6dddb-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6dddb-370">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="6dddb-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="6dddb-372">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6dddb-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6dddb-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6dddb-374">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="6dddb-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6dddb-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="6dddb-376">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6dddb-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6dddb-377">AzureRM.Automation</span></span>
* <span data-ttu-id="6dddb-378">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="6dddb-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="6dddb-379">AzureRM.Backup</span></span>
* <span data-ttu-id="6dddb-380">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6dddb-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6dddb-381">AzureRM.Batch</span></span>
* <span data-ttu-id="6dddb-382">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="6dddb-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="6dddb-383">AzureRM.Billing</span></span>
* <span data-ttu-id="6dddb-384">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="6dddb-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="6dddb-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="6dddb-386">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="6dddb-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="6dddb-388">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-389">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-390">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6dddb-391">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="6dddb-392">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="6dddb-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="6dddb-393">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6dddb-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6dddb-394">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="6dddb-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6dddb-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6dddb-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="6dddb-396">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="6dddb-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6dddb-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="6dddb-398">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="6dddb-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6dddb-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="6dddb-400">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="6dddb-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="6dddb-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="6dddb-402">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6dddb-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6dddb-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6dddb-404">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6dddb-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6dddb-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6dddb-406">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6dddb-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6dddb-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6dddb-408">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="6dddb-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="6dddb-409">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6dddb-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6dddb-410">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6dddb-411">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="6dddb-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6dddb-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="6dddb-413">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="6dddb-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="6dddb-414">AzureRM.Dns</span></span>
* <span data-ttu-id="6dddb-415">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6dddb-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6dddb-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6dddb-417">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6dddb-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="6dddb-419">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="6dddb-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6dddb-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="6dddb-421">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6dddb-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6dddb-422">AzureRM.Insights</span></span>
* <span data-ttu-id="6dddb-423">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="6dddb-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="6dddb-425">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-427">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6dddb-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6dddb-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6dddb-429">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="6dddb-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6dddb-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="6dddb-431">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="6dddb-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6dddb-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="6dddb-433">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="6dddb-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6dddb-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="6dddb-435">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="6dddb-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="6dddb-436">AzureRM.Media</span></span>
* <span data-ttu-id="6dddb-437">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-438">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-439">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="6dddb-440">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dddb-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6dddb-441">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6dddb-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="6dddb-442">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6dddb-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6dddb-443">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6dddb-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="6dddb-444">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6dddb-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6dddb-445">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="6dddb-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="6dddb-446">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="6dddb-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="6dddb-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6dddb-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="6dddb-448">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="6dddb-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6dddb-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6dddb-450">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6dddb-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6dddb-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6dddb-452">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="6dddb-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6dddb-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="6dddb-454">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="6dddb-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="6dddb-456">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6dddb-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6dddb-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6dddb-458">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="6dddb-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="6dddb-459">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="6dddb-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="6dddb-460">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="6dddb-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="6dddb-461">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="6dddb-462">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6dddb-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="6dddb-463">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="6dddb-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="6dddb-464">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="6dddb-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="6dddb-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6dddb-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6dddb-466">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="6dddb-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6dddb-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="6dddb-468">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6dddb-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6dddb-469">AzureRM.Relay</span></span>
* <span data-ttu-id="6dddb-470">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-471">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-472">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6dddb-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="6dddb-473">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6dddb-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="6dddb-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="6dddb-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="6dddb-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="6dddb-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="6dddb-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="6dddb-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6dddb-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="6dddb-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="6dddb-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="6dddb-481">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6dddb-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="6dddb-482">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="6dddb-483">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6dddb-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6dddb-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6dddb-485">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-487">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6dddb-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6dddb-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6dddb-489">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-490">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-491">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6dddb-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-492">AzureRM.Storage</span></span>
* <span data-ttu-id="6dddb-493">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="6dddb-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="6dddb-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="6dddb-495">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6dddb-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6dddb-496">AzureRM.Tags</span></span>
* <span data-ttu-id="6dddb-497">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6dddb-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6dddb-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6dddb-499">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="6dddb-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="6dddb-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="6dddb-501">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-502">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-503">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="6dddb-504">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6dddb-505">Geral</span><span class="sxs-lookup"><span data-stu-id="6dddb-505">General</span></span>
* <span data-ttu-id="6dddb-506">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="6dddb-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-507">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-507">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-508">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="6dddb-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="6dddb-509">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6dddb-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-510">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-511">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dddb-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="6dddb-512">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6dddb-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6dddb-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6dddb-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6dddb-514">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6dddb-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6dddb-515">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="6dddb-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6dddb-516">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6dddb-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6dddb-517">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="6dddb-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6dddb-518">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6dddb-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6dddb-519">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="6dddb-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-520">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-521">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="6dddb-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6dddb-522">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6dddb-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6dddb-523">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="6dddb-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6dddb-524">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="6dddb-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6dddb-525">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="6dddb-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6dddb-526">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="6dddb-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6dddb-527">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6dddb-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6dddb-528">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="6dddb-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6dddb-529">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6dddb-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6dddb-530">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="6dddb-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6dddb-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6dddb-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6dddb-532">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6dddb-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6dddb-533">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="6dddb-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6dddb-534">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6dddb-535">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6dddb-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6dddb-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6dddb-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6dddb-537">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="6dddb-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6dddb-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="6dddb-539">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="6dddb-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6dddb-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6dddb-540">AzureRM.Insights</span></span>
* <span data-ttu-id="6dddb-541">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="6dddb-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6dddb-542">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="6dddb-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-544">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-545">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-546">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="6dddb-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-547">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-548">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6dddb-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6dddb-549">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6dddb-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-551">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="6dddb-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6dddb-552">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="6dddb-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-553">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-554">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6dddb-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6dddb-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6dddb-556">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6dddb-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6dddb-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6dddb-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6dddb-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6dddb-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6dddb-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6dddb-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6dddb-560">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6dddb-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6dddb-561">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6dddb-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6dddb-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-562">AzureRM.Storage</span></span>
* <span data-ttu-id="6dddb-563">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="6dddb-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6dddb-564">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="6dddb-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6dddb-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6dddb-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6dddb-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6dddb-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6dddb-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6dddb-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6dddb-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6dddb-568">AzureRM.Tags</span></span>
* <span data-ttu-id="6dddb-569">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="6dddb-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6dddb-570">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-571">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-571">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-572">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="6dddb-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6dddb-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-573">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-574">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="6dddb-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6dddb-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6dddb-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6dddb-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6dddb-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6dddb-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6dddb-578">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="6dddb-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6dddb-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6dddb-579">AzureRM.Automation</span></span>
* <span data-ttu-id="6dddb-580">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="6dddb-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-581">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-582">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6dddb-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6dddb-583">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="6dddb-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6dddb-584">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="6dddb-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6dddb-585">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="6dddb-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6dddb-586">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="6dddb-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6dddb-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="6dddb-588">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-590">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6dddb-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6dddb-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6dddb-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6dddb-592">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6dddb-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-593">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-594">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dddb-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6dddb-595">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="6dddb-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6dddb-596">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="6dddb-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6dddb-597">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6dddb-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6dddb-598">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6dddb-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6dddb-599">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="6dddb-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6dddb-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6dddb-600">AzureRM.Relay</span></span>
* <span data-ttu-id="6dddb-601">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="6dddb-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-602">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-603">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="6dddb-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6dddb-604">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="6dddb-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6dddb-605">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6dddb-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6dddb-606">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6dddb-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6dddb-607">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="6dddb-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-609">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="6dddb-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6dddb-610">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="6dddb-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6dddb-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6dddb-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6dddb-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6dddb-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6dddb-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6dddb-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6dddb-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6dddb-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6dddb-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6dddb-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6dddb-616">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6dddb-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6dddb-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6dddb-618">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="6dddb-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-619">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-620">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="6dddb-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6dddb-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6dddb-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-623">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-624">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="6dddb-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6dddb-625">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="6dddb-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6dddb-626">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="6dddb-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6dddb-627">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6dddb-628">Geral</span><span class="sxs-lookup"><span data-stu-id="6dddb-628">General</span></span>
* <span data-ttu-id="6dddb-629">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="6dddb-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-630">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-630">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-631">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="6dddb-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-632">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-633">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="6dddb-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6dddb-634">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6dddb-635">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6dddb-636">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="6dddb-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6dddb-637">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6dddb-638">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6dddb-639">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6dddb-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6dddb-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6dddb-641">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="6dddb-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6dddb-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6dddb-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6dddb-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6dddb-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6dddb-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6dddb-646">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6dddb-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6dddb-647">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6dddb-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6dddb-648">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="6dddb-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6dddb-649">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="6dddb-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6dddb-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6dddb-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="6dddb-651">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6dddb-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6dddb-652">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="6dddb-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6dddb-653">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="6dddb-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6dddb-654">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6dddb-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-656">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="6dddb-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-657">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-658">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6dddb-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6dddb-659">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="6dddb-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6dddb-660">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6dddb-661">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6dddb-662">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6dddb-663">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6dddb-664">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6dddb-665">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6dddb-666">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6dddb-667">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="6dddb-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6dddb-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6dddb-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6dddb-669">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="6dddb-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6dddb-670">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="6dddb-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6dddb-671">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="6dddb-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-672">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-673">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="6dddb-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6dddb-674">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6dddb-675">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6dddb-676">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dddb-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6dddb-677">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6dddb-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6dddb-678">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6dddb-679">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="6dddb-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6dddb-680">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6dddb-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6dddb-681">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6dddb-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6dddb-682">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="6dddb-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6dddb-683">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="6dddb-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6dddb-684">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="6dddb-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6dddb-685">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="6dddb-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6dddb-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6dddb-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6dddb-687">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6dddb-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-688">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-689">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6dddb-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6dddb-690">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="6dddb-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6dddb-691">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-692">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-692">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-693">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="6dddb-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6dddb-694">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="6dddb-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6dddb-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6dddb-695">Azure.Storage</span></span>
* <span data-ttu-id="6dddb-696">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="6dddb-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-697">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-698">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="6dddb-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6dddb-699">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="6dddb-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6dddb-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6dddb-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6dddb-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6dddb-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6dddb-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6dddb-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6dddb-703">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="6dddb-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6dddb-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6dddb-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6dddb-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6dddb-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6dddb-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6dddb-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6dddb-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6dddb-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6dddb-708">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6dddb-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6dddb-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6dddb-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6dddb-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6dddb-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6dddb-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6dddb-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6dddb-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6dddb-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6dddb-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6dddb-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6dddb-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6dddb-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6dddb-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6dddb-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6dddb-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6dddb-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6dddb-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6dddb-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6dddb-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6dddb-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6dddb-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6dddb-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6dddb-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6dddb-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6dddb-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6dddb-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6dddb-724">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="6dddb-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-726">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6dddb-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6dddb-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6dddb-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6dddb-728">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="6dddb-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6dddb-729">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="6dddb-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6dddb-730">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6dddb-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6dddb-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6dddb-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6dddb-732">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="6dddb-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6dddb-733">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6dddb-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-734">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-735">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6dddb-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6dddb-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6dddb-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6dddb-737">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-738">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-739">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6dddb-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6dddb-740">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="6dddb-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6dddb-741">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6dddb-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6dddb-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6dddb-743">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="6dddb-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6dddb-744">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-745">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-745">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-746">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="6dddb-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6dddb-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6dddb-747">AzureRM.Compute</span></span>
* <span data-ttu-id="6dddb-748">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="6dddb-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6dddb-749">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="6dddb-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6dddb-750">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="6dddb-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6dddb-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6dddb-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6dddb-752">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="6dddb-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6dddb-753">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="6dddb-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6dddb-754">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="6dddb-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6dddb-755">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="6dddb-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6dddb-756">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="6dddb-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6dddb-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6dddb-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6dddb-758">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="6dddb-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-759">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-760">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="6dddb-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6dddb-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6dddb-761">AzureRM.Resources</span></span>
* <span data-ttu-id="6dddb-762">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="6dddb-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6dddb-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6dddb-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6dddb-764">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="6dddb-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6dddb-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-765">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-766">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="6dddb-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6dddb-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6dddb-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6dddb-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6dddb-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6dddb-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6dddb-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6dddb-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6dddb-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6dddb-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6dddb-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6dddb-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6dddb-772">AzureRM.Websites</span></span>
* <span data-ttu-id="6dddb-773">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="6dddb-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6dddb-774">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="6dddb-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6dddb-775">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="6dddb-775">AzureRM.Profile</span></span>
* <span data-ttu-id="6dddb-776">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="6dddb-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6dddb-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6dddb-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6dddb-778">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="6dddb-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6dddb-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6dddb-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6dddb-780">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="6dddb-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6dddb-781">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6dddb-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6dddb-782">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="6dddb-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6dddb-783">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="6dddb-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6dddb-784">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="6dddb-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6dddb-785">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="6dddb-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6dddb-786">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="6dddb-786">Added support for MSI identity</span></span>
* <span data-ttu-id="6dddb-787">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="6dddb-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6dddb-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6dddb-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6dddb-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6dddb-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6dddb-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6dddb-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6dddb-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6dddb-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6dddb-792">AzureRM.Batch</span></span>
* <span data-ttu-id="6dddb-793">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6dddb-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6dddb-794">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6dddb-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6dddb-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6dddb-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="6dddb-796">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="6dddb-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6dddb-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6dddb-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6dddb-798">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6dddb-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6dddb-799">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6dddb-800">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6dddb-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6dddb-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6dddb-801">AzureRM.Network</span></span>
* <span data-ttu-id="6dddb-802">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6dddb-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6dddb-803">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="6dddb-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6dddb-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dddb-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6dddb-805">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="6dddb-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6dddb-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6dddb-807">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="6dddb-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6dddb-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6dddb-809">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="6dddb-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6dddb-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6dddb-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6dddb-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6dddb-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6dddb-812">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="6dddb-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6dddb-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6dddb-813">AzureRM.Sql</span></span>
* <span data-ttu-id="6dddb-814">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="6dddb-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6dddb-815">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="6dddb-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6dddb-816">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="6dddb-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6dddb-817">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="6dddb-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6dddb-818">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="6dddb-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6dddb-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6dddb-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6dddb-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6dddb-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6dddb-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6dddb-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6dddb-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6dddb-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6dddb-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6dddb-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6dddb-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6dddb-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6dddb-825">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="6dddb-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
