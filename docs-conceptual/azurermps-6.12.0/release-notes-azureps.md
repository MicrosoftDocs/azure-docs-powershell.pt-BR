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
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275513"
---
# <a name="release-notes"></a><span data-ttu-id="827d0-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="827d0-103">Release notes</span></span>

<span data-ttu-id="827d0-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="827d0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="827d0-105">6.12.0 - novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-106">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-107">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="827d0-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="827d0-108">Renomear o parâmetro TenantId no cmdlet Connect-AzureRmAccount do locatário e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="827d0-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="827d0-109">Descrição de TenantId atualizada para Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="827d0-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="827d0-110">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="827d0-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="827d0-111">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="827d0-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="827d0-112">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="827d0-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="827d0-113">Corrigir o problema em que 'Disconnect-AzureRmAccount' seria lançado se não conectado</span><span class="sxs-lookup"><span data-stu-id="827d0-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="827d0-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="827d0-114">AzureRM.Automation</span></span>
* <span data-ttu-id="827d0-115">Nome do arquivo DLL de cmdlet renomeado para Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="827d0-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="827d0-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="827d0-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="827d0-117">Adicionar operação Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="827d0-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-118">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-119">Adicionar cmdlets Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="827d0-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="827d0-120">Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="827d0-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="827d0-121">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzureRmVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="827d0-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-123">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="827d0-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="827d0-124">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="827d0-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="827d0-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="827d0-125">AzureRM.Insights</span></span>
* <span data-ttu-id="827d0-126">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="827d0-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="827d0-127">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="827d0-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="827d0-128">Correção do problema #7513 [Insights] Set-AzureRMDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="827d0-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="827d0-129">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="827d0-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-130">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-131">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="827d0-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="827d0-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="827d0-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="827d0-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="827d0-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="827d0-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="827d0-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="827d0-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="827d0-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="827d0-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="827d0-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="827d0-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="827d0-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="827d0-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="827d0-139">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="827d0-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="827d0-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="827d0-141">Adicionado suporte para compartilhamentos de arquivos do Azure nos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="827d0-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-142">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-143">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="827d0-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="827d0-144">Permitir a listagem de recursos usando o parâmetro '-ResourceId' para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="827d0-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-146">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="827d0-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="827d0-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="827d0-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="827d0-148">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="827d0-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="827d0-149">Corrigir 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="827d0-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="827d0-150">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="827d0-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="827d0-151">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="827d0-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="827d0-152">Corrigir 'Update-AzureRmServiceFabricDurability' para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="827d0-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="827d0-153">6.11.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-154">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-154">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-155">Corrigir o problema com Get-AzureRmSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="827d0-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="827d0-156">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="827d0-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="827d0-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-157">AzureRM.Backup</span></span>
* <span data-ttu-id="827d0-158">Cmdlets do Backup do Azure preteridos.</span><span class="sxs-lookup"><span data-stu-id="827d0-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-159">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-160">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para 'New-AzureRmVm'</span><span class="sxs-lookup"><span data-stu-id="827d0-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="827d0-161">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="827d0-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-163">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="827d0-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="827d0-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: obtém ou lista regras de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="827d0-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="827d0-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: adiciona uma regra de rede virtual para a conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="827d0-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="827d0-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="827d0-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="827d0-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="827d0-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-168">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-169">Atualize o cmdlet Test-AzureRmNetworkWatcherConnectivity, passe o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="827d0-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="827d0-170">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="827d0-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-171">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-172">Corrija o problema onde Get-AzureRMRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="827d0-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="827d0-173">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="827d0-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="827d0-174">6.10.0 – outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="827d0-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-175">Azure.Storage</span></span>
* <span data-ttu-id="827d0-176">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="827d0-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="827d0-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="827d0-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="827d0-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="827d0-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="827d0-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="827d0-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="827d0-180">Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="827d0-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-181">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-182">Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="827d0-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="827d0-183">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="827d0-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="827d0-184">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="827d0-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="827d0-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="827d0-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="827d0-186">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="827d0-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-187">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-188">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="827d0-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="827d0-189">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="827d0-189">new cmdlets added</span></span>
    - <span data-ttu-id="827d0-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="827d0-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="827d0-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="827d0-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="827d0-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="827d0-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="827d0-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="827d0-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="827d0-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="827d0-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="827d0-196">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="827d0-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="827d0-197">Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="827d0-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="827d0-198">Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="827d0-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="827d0-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="827d0-200">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="827d0-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="827d0-201">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="827d0-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-202">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-203">Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="827d0-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="827d0-204">Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="827d0-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-205">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-206">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="827d0-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="827d0-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-207">AzureRM.Storage</span></span>
* <span data-ttu-id="827d0-208">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="827d0-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="827d0-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="827d0-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-210">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-211">Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="827d0-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="827d0-212">Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="827d0-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="827d0-213">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="827d0-214">Geral</span><span class="sxs-lookup"><span data-stu-id="827d0-214">General</span></span>
* <span data-ttu-id="827d0-215">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="827d0-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="827d0-216">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-216">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-217">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="827d0-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="827d0-218">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="827d0-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="827d0-219">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="827d0-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="827d0-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-220">Azure.Storage</span></span>
* <span data-ttu-id="827d0-221">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="827d0-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="827d0-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="827d0-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="827d0-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="827d0-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="827d0-224">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="827d0-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-225">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-226">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="827d0-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="827d0-227">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="827d0-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="827d0-228">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="827d0-229">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="827d0-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="827d0-230">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="827d0-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="827d0-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="827d0-231">AzureRM.Dns</span></span>
* <span data-ttu-id="827d0-232">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="827d0-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="827d0-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="827d0-233">AzureRM.Insights</span></span>
* <span data-ttu-id="827d0-234">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="827d0-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="827d0-235">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="827d0-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="827d0-236">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="827d0-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="827d0-237">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="827d0-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="827d0-238">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="827d0-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-239">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-240">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="827d0-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="827d0-241">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="827d0-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="827d0-242">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="827d0-243">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="827d0-244">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="827d0-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="827d0-245">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="827d0-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="827d0-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="827d0-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="827d0-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="827d0-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="827d0-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="827d0-251">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="827d0-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="827d0-252">Novos cmdlets adicionados para o recurso: Firewall do Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="827d0-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="827d0-253">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="827d0-254">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="827d0-255">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="827d0-256">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="827d0-257">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="827d0-258">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="827d0-259">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="827d0-260">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="827d0-261">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="827d0-262">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="827d0-263">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="827d0-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="827d0-264">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="827d0-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="827d0-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="827d0-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="827d0-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="827d0-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="827d0-274">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="827d0-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="827d0-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="827d0-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="827d0-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="827d0-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="827d0-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="827d0-279">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="827d0-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="827d0-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="827d0-282">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="827d0-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="827d0-283">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="827d0-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="827d0-284">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="827d0-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="827d0-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="827d0-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="827d0-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="827d0-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="827d0-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="827d0-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="827d0-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="827d0-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="827d0-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="827d0-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="827d0-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="827d0-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="827d0-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="827d0-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="827d0-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="827d0-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="827d0-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="827d0-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="827d0-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="827d0-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="827d0-304">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="827d0-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="827d0-305">New-AzureRmDelegation: cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="827d0-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="827d0-306">Remove-AzureRmDelegation: usa uma sub-rede e remove o nome de delegação fornecido dela</span><span class="sxs-lookup"><span data-stu-id="827d0-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="827d0-307">Add-AzureRmDelegation: usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação para essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="827d0-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="827d0-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="827d0-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="827d0-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="827d0-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="827d0-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="827d0-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="827d0-311">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="827d0-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="827d0-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="827d0-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="827d0-313">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="827d0-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-314">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-315">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="827d0-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="827d0-316">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="827d0-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="827d0-317">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="827d0-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="827d0-318">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="827d0-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="827d0-319">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="827d0-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-321">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="827d0-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="827d0-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="827d0-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="827d0-323">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="827d0-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="827d0-324">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="827d0-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="827d0-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-325">AzureRM.Storage</span></span>
* <span data-ttu-id="827d0-326">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="827d0-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="827d0-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="827d0-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="827d0-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="827d0-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="827d0-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="827d0-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="827d0-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="827d0-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="827d0-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="827d0-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="827d0-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="827d0-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="827d0-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="827d0-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="827d0-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="827d0-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="827d0-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-338">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-339">Dois novos cmdlets adicionados: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="827d0-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="827d0-340">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="827d0-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="827d0-341">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="827d0-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="827d0-342">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="827d0-343">Geral</span><span class="sxs-lookup"><span data-stu-id="827d0-343">General</span></span>
* <span data-ttu-id="827d0-344">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="827d0-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="827d0-345">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="827d0-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="827d0-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="827d0-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="827d0-347">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="827d0-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="827d0-348">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="827d0-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="827d0-349">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="827d0-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="827d0-350">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="827d0-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="827d0-351">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="827d0-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="827d0-352">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="827d0-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="827d0-353">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="827d0-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="827d0-354">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="827d0-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="827d0-355">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="827d0-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="827d0-356">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="827d0-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="827d0-357">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="827d0-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="827d0-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-358">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-359">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="827d0-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="827d0-360">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="827d0-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="827d0-361">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="827d0-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="827d0-362">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="827d0-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-363">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-364">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="827d0-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="827d0-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="827d0-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="827d0-366">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="827d0-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="827d0-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-367">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-368">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="827d0-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-370">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="827d0-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="827d0-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="827d0-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="827d0-372">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="827d0-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="827d0-373">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="827d0-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="827d0-374">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="827d0-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="827d0-375">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="827d0-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="827d0-376">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="827d0-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="827d0-377">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="827d0-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="827d0-378">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="827d0-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="827d0-379">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="827d0-380">Geral</span><span class="sxs-lookup"><span data-stu-id="827d0-380">General</span></span>
* <span data-ttu-id="827d0-381">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="827d0-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="827d0-382">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-382">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-383">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="827d0-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-384">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-385">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="827d0-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="827d0-386">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="827d0-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="827d0-387">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="827d0-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="827d0-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="827d0-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="827d0-389">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="827d0-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-390">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-391">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="827d0-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="827d0-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="827d0-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="827d0-393">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="827d0-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-394">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-395">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="827d0-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-397">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="827d0-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="827d0-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="827d0-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="827d0-399">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="827d0-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="827d0-400">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="827d0-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="827d0-401">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="827d0-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="827d0-402">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="827d0-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="827d0-403">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="827d0-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="827d0-404">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="827d0-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="827d0-405">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="827d0-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-406">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-407">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="827d0-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="827d0-408">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-409">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-409">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-410">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="827d0-411">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="827d0-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="827d0-412">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="827d0-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="827d0-413">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="827d0-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="827d0-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-414">Azure.Storage</span></span>
* <span data-ttu-id="827d0-415">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="827d0-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="827d0-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="827d0-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="827d0-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="827d0-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="827d0-418">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="827d0-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="827d0-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="827d0-420">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="827d0-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="827d0-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="827d0-422">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="827d0-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="827d0-424">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="827d0-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="827d0-425">AzureRM.Automation</span></span>
* <span data-ttu-id="827d0-426">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="827d0-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-427">AzureRM.Backup</span></span>
* <span data-ttu-id="827d0-428">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="827d0-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="827d0-429">AzureRM.Batch</span></span>
* <span data-ttu-id="827d0-430">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="827d0-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="827d0-431">AzureRM.Billing</span></span>
* <span data-ttu-id="827d0-432">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="827d0-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="827d0-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="827d0-434">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="827d0-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="827d0-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="827d0-436">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-437">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-438">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="827d0-439">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="827d0-440">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="827d0-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="827d0-441">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="827d0-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="827d0-442">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="827d0-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="827d0-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="827d0-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="827d0-444">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="827d0-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="827d0-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="827d0-446">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="827d0-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="827d0-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="827d0-448">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="827d0-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="827d0-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="827d0-450">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="827d0-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="827d0-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="827d0-452">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="827d0-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="827d0-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="827d0-454">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-456">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="827d0-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="827d0-457">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="827d0-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="827d0-458">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="827d0-459">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="827d0-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="827d0-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="827d0-461">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="827d0-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="827d0-462">AzureRM.Dns</span></span>
* <span data-ttu-id="827d0-463">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="827d0-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="827d0-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="827d0-465">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="827d0-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="827d0-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="827d0-467">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="827d0-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="827d0-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="827d0-469">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="827d0-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="827d0-470">AzureRM.Insights</span></span>
* <span data-ttu-id="827d0-471">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="827d0-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="827d0-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="827d0-473">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-475">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="827d0-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="827d0-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="827d0-477">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="827d0-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="827d0-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="827d0-479">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="827d0-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="827d0-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="827d0-481">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="827d0-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="827d0-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="827d0-483">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="827d0-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="827d0-484">AzureRM.Media</span></span>
* <span data-ttu-id="827d0-485">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-486">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-487">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="827d0-488">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="827d0-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="827d0-489">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="827d0-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="827d0-490">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="827d0-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="827d0-491">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="827d0-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="827d0-492">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="827d0-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="827d0-493">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="827d0-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="827d0-494">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="827d0-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="827d0-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="827d0-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="827d0-496">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="827d0-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="827d0-498">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="827d0-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="827d0-500">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="827d0-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="827d0-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="827d0-502">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="827d0-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="827d0-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="827d0-504">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="827d0-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="827d0-506">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="827d0-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="827d0-507">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="827d0-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="827d0-508">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="827d0-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="827d0-509">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="827d0-510">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="827d0-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="827d0-511">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="827d0-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="827d0-512">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="827d0-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="827d0-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="827d0-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="827d0-514">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="827d0-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="827d0-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="827d0-516">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="827d0-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="827d0-517">AzureRM.Relay</span></span>
* <span data-ttu-id="827d0-518">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-519">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-520">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="827d0-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="827d0-521">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="827d0-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="827d0-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="827d0-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="827d0-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="827d0-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="827d0-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="827d0-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="827d0-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="827d0-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="827d0-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="827d0-529">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="827d0-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="827d0-530">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="827d0-531">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="827d0-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="827d0-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="827d0-533">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-535">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="827d0-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="827d0-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="827d0-537">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-538">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-539">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="827d0-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-540">AzureRM.Storage</span></span>
* <span data-ttu-id="827d0-541">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="827d0-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="827d0-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="827d0-543">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="827d0-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="827d0-544">AzureRM.Tags</span></span>
* <span data-ttu-id="827d0-545">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="827d0-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="827d0-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="827d0-547">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="827d0-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="827d0-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="827d0-549">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-550">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-551">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="827d0-552">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="827d0-553">Geral</span><span class="sxs-lookup"><span data-stu-id="827d0-553">General</span></span>
* <span data-ttu-id="827d0-554">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="827d0-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="827d0-555">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-555">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-556">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="827d0-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="827d0-557">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="827d0-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-558">Azure.Storage</span></span>
* <span data-ttu-id="827d0-559">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827d0-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="827d0-560">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="827d0-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="827d0-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="827d0-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="827d0-562">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="827d0-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="827d0-563">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="827d0-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="827d0-564">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="827d0-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="827d0-565">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="827d0-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="827d0-566">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="827d0-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="827d0-567">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="827d0-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-568">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-569">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="827d0-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="827d0-570">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="827d0-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="827d0-571">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="827d0-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="827d0-572">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="827d0-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="827d0-573">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="827d0-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="827d0-574">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="827d0-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="827d0-575">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="827d0-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="827d0-576">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="827d0-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="827d0-577">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="827d0-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="827d0-578">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="827d0-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="827d0-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="827d0-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="827d0-580">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="827d0-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="827d0-581">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="827d0-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="827d0-582">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="827d0-583">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="827d0-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-585">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="827d0-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="827d0-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="827d0-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="827d0-587">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="827d0-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="827d0-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="827d0-588">AzureRM.Insights</span></span>
* <span data-ttu-id="827d0-589">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="827d0-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="827d0-590">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="827d0-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-592">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-593">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-594">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="827d0-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-595">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-596">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="827d0-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="827d0-597">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="827d0-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-599">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="827d0-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="827d0-600">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="827d0-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="827d0-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-601">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-602">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="827d0-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="827d0-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="827d0-604">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="827d0-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="827d0-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="827d0-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="827d0-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="827d0-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="827d0-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="827d0-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="827d0-608">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="827d0-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="827d0-609">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="827d0-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="827d0-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-610">AzureRM.Storage</span></span>
* <span data-ttu-id="827d0-611">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="827d0-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="827d0-612">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="827d0-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="827d0-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="827d0-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="827d0-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="827d0-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="827d0-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="827d0-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="827d0-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="827d0-616">AzureRM.Tags</span></span>
* <span data-ttu-id="827d0-617">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="827d0-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="827d0-618">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-619">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-619">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-620">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="827d0-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="827d0-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-621">Azure.Storage</span></span>
* <span data-ttu-id="827d0-622">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="827d0-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="827d0-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="827d0-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="827d0-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="827d0-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="827d0-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="827d0-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="827d0-626">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="827d0-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="827d0-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="827d0-627">AzureRM.Automation</span></span>
* <span data-ttu-id="827d0-628">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="827d0-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-629">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-630">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827d0-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="827d0-631">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="827d0-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="827d0-632">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="827d0-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="827d0-633">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="827d0-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="827d0-634">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="827d0-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="827d0-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="827d0-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="827d0-636">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="827d0-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-638">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="827d0-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="827d0-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="827d0-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="827d0-640">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="827d0-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-641">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-642">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="827d0-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="827d0-643">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="827d0-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="827d0-644">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="827d0-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="827d0-645">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="827d0-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="827d0-646">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="827d0-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="827d0-647">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="827d0-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="827d0-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="827d0-648">AzureRM.Relay</span></span>
* <span data-ttu-id="827d0-649">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="827d0-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-650">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-651">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="827d0-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="827d0-652">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="827d0-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="827d0-653">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="827d0-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="827d0-654">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="827d0-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="827d0-655">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="827d0-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-657">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="827d0-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="827d0-658">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="827d0-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="827d0-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="827d0-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="827d0-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="827d0-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="827d0-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="827d0-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="827d0-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="827d0-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="827d0-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="827d0-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="827d0-664">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="827d0-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="827d0-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="827d0-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="827d0-666">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="827d0-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-667">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-668">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="827d0-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="827d0-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="827d0-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-671">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-672">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="827d0-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="827d0-673">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="827d0-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="827d0-674">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="827d0-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="827d0-675">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="827d0-676">Geral</span><span class="sxs-lookup"><span data-stu-id="827d0-676">General</span></span>
* <span data-ttu-id="827d0-677">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="827d0-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="827d0-678">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-678">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-679">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="827d0-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-680">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-681">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="827d0-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="827d0-682">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="827d0-683">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="827d0-684">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="827d0-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="827d0-685">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="827d0-686">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="827d0-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="827d0-687">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="827d0-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="827d0-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="827d0-689">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="827d0-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="827d0-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="827d0-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="827d0-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-694">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="827d0-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="827d0-695">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="827d0-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="827d0-696">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="827d0-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="827d0-697">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="827d0-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="827d0-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="827d0-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="827d0-699">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="827d0-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="827d0-700">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="827d0-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="827d0-701">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="827d0-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="827d0-702">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="827d0-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-704">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="827d0-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-705">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-706">Expor novas Skus para VirtualNetworkGateways com Redundância de Zona</span><span class="sxs-lookup"><span data-stu-id="827d0-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="827d0-707">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="827d0-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="827d0-708">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="827d0-709">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="827d0-710">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="827d0-711">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="827d0-712">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="827d0-713">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="827d0-714">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="827d0-715">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="827d0-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="827d0-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="827d0-717">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="827d0-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="827d0-718">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="827d0-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="827d0-719">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="827d0-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-720">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-721">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="827d0-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="827d0-722">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="827d0-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="827d0-723">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="827d0-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="827d0-724">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="827d0-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="827d0-725">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="827d0-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="827d0-726">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="827d0-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="827d0-727">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="827d0-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="827d0-728">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="827d0-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="827d0-729">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="827d0-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="827d0-730">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="827d0-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="827d0-731">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="827d0-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="827d0-732">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="827d0-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="827d0-733">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="827d0-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="827d0-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="827d0-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="827d0-735">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="827d0-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-736">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-737">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="827d0-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="827d0-738">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="827d0-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="827d0-739">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-740">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-740">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-741">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="827d0-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="827d0-742">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="827d0-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="827d0-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="827d0-743">Azure.Storage</span></span>
* <span data-ttu-id="827d0-744">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="827d0-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-745">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-746">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="827d0-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="827d0-747">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="827d0-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="827d0-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="827d0-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="827d0-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="827d0-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="827d0-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="827d0-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="827d0-751">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="827d0-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="827d0-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="827d0-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="827d0-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="827d0-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="827d0-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="827d0-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="827d0-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="827d0-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="827d0-756">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="827d0-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="827d0-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="827d0-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="827d0-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="827d0-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="827d0-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="827d0-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="827d0-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="827d0-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="827d0-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="827d0-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="827d0-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="827d0-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="827d0-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="827d0-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="827d0-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="827d0-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="827d0-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="827d0-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="827d0-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="827d0-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="827d0-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="827d0-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="827d0-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827d0-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="827d0-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="827d0-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="827d0-772">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="827d0-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-774">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="827d0-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="827d0-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="827d0-776">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="827d0-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="827d0-777">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="827d0-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="827d0-778">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="827d0-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="827d0-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="827d0-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="827d0-780">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="827d0-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="827d0-781">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="827d0-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-782">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-783">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="827d0-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="827d0-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="827d0-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="827d0-785">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-786">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-787">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="827d0-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="827d0-788">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="827d0-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="827d0-789">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="827d0-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="827d0-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="827d0-791">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="827d0-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="827d0-792">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-793">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-793">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-794">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="827d0-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="827d0-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="827d0-795">AzureRM.Compute</span></span>
* <span data-ttu-id="827d0-796">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="827d0-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="827d0-797">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="827d0-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="827d0-798">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="827d0-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="827d0-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="827d0-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="827d0-800">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="827d0-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="827d0-801">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="827d0-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="827d0-802">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="827d0-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="827d0-803">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="827d0-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="827d0-804">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="827d0-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="827d0-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="827d0-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="827d0-806">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="827d0-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="827d0-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-807">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-808">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="827d0-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="827d0-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="827d0-809">AzureRM.Resources</span></span>
* <span data-ttu-id="827d0-810">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="827d0-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="827d0-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="827d0-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="827d0-812">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="827d0-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="827d0-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-813">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-814">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="827d0-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="827d0-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="827d0-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="827d0-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="827d0-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="827d0-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="827d0-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="827d0-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="827d0-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="827d0-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="827d0-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="827d0-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="827d0-820">AzureRM.Websites</span></span>
* <span data-ttu-id="827d0-821">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="827d0-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="827d0-822">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="827d0-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="827d0-823">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="827d0-823">AzureRM.Profile</span></span>
* <span data-ttu-id="827d0-824">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="827d0-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="827d0-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="827d0-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="827d0-826">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="827d0-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="827d0-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="827d0-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="827d0-828">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="827d0-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="827d0-829">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="827d0-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="827d0-830">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="827d0-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="827d0-831">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="827d0-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="827d0-832">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="827d0-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="827d0-833">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="827d0-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="827d0-834">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="827d0-834">Added support for MSI identity</span></span>
* <span data-ttu-id="827d0-835">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="827d0-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="827d0-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="827d0-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="827d0-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="827d0-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="827d0-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="827d0-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="827d0-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="827d0-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="827d0-840">AzureRM.Batch</span></span>
* <span data-ttu-id="827d0-841">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="827d0-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="827d0-842">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="827d0-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="827d0-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="827d0-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="827d0-844">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="827d0-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="827d0-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="827d0-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="827d0-846">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="827d0-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="827d0-847">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="827d0-848">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="827d0-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="827d0-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="827d0-849">AzureRM.Network</span></span>
* <span data-ttu-id="827d0-850">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="827d0-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="827d0-851">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="827d0-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="827d0-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="827d0-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="827d0-853">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="827d0-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="827d0-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="827d0-855">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="827d0-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="827d0-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="827d0-857">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="827d0-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="827d0-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="827d0-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="827d0-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="827d0-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="827d0-860">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="827d0-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="827d0-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="827d0-861">AzureRM.Sql</span></span>
* <span data-ttu-id="827d0-862">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="827d0-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="827d0-863">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="827d0-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="827d0-864">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="827d0-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="827d0-865">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="827d0-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="827d0-866">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="827d0-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="827d0-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="827d0-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="827d0-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="827d0-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="827d0-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="827d0-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="827d0-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="827d0-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="827d0-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="827d0-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="827d0-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="827d0-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="827d0-873">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="827d0-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
