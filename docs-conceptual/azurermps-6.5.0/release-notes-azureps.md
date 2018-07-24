---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110476"
---
# <a name="release-notes"></a><span data-ttu-id="0126b-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="0126b-103">Release notes</span></span>

<span data-ttu-id="0126b-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0126b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="0126b-105">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0126b-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="0126b-106">AzureRM.Profile</span></span>
* <span data-ttu-id="0126b-107">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="0126b-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0126b-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0126b-108">Azure.Storage</span></span>
* <span data-ttu-id="0126b-109">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="0126b-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="0126b-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0126b-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="0126b-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0126b-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0126b-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0126b-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0126b-113">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="0126b-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="0126b-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0126b-114">AzureRM.Automation</span></span>
* <span data-ttu-id="0126b-115">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="0126b-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0126b-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0126b-116">AzureRM.Compute</span></span>
* <span data-ttu-id="0126b-117">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0126b-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="0126b-118">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="0126b-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0126b-119">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="0126b-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0126b-120">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="0126b-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="0126b-121">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="0126b-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0126b-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0126b-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="0126b-123">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="0126b-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0126b-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0126b-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0126b-125">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0126b-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="0126b-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0126b-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="0126b-127">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0126b-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0126b-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0126b-128">AzureRM.Network</span></span>
* <span data-ttu-id="0126b-129">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0126b-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="0126b-130">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="0126b-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="0126b-131">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="0126b-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="0126b-132">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="0126b-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="0126b-133">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="0126b-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="0126b-134">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="0126b-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="0126b-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="0126b-135">AzureRM.Relay</span></span>
* <span data-ttu-id="0126b-136">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="0126b-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0126b-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0126b-137">AzureRM.Resources</span></span>
* <span data-ttu-id="0126b-138">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="0126b-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="0126b-139">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="0126b-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="0126b-140">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0126b-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="0126b-141">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0126b-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="0126b-142">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="0126b-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0126b-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0126b-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0126b-144">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="0126b-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="0126b-145">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="0126b-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="0126b-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0126b-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0126b-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0126b-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0126b-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0126b-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0126b-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0126b-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0126b-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0126b-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="0126b-151">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="0126b-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0126b-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0126b-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0126b-153">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="0126b-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0126b-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0126b-154">AzureRM.Sql</span></span>
* <span data-ttu-id="0126b-155">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="0126b-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="0126b-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0126b-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="0126b-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0126b-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0126b-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0126b-158">AzureRM.Websites</span></span>
* <span data-ttu-id="0126b-159">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="0126b-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="0126b-160">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="0126b-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="0126b-161">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="0126b-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="0126b-162">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0126b-163">Geral</span><span class="sxs-lookup"><span data-stu-id="0126b-163">General</span></span>
* <span data-ttu-id="0126b-164">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="0126b-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0126b-165">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="0126b-165">AzureRM.Profile</span></span>
* <span data-ttu-id="0126b-166">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="0126b-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0126b-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0126b-167">AzureRM.Compute</span></span>
* <span data-ttu-id="0126b-168">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="0126b-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="0126b-169">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="0126b-170">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="0126b-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="0126b-171">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="0126b-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="0126b-172">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="0126b-173">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="0126b-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="0126b-174">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0126b-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0126b-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0126b-176">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="0126b-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="0126b-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0126b-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0126b-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0126b-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0126b-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0126b-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0126b-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0126b-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0126b-181">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0126b-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0126b-182">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0126b-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0126b-183">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="0126b-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="0126b-184">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="0126b-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0126b-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0126b-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="0126b-186">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0126b-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="0126b-187">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="0126b-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="0126b-188">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="0126b-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="0126b-189">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0126b-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0126b-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0126b-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0126b-191">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="0126b-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0126b-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0126b-192">AzureRM.Network</span></span>
* <span data-ttu-id="0126b-193">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0126b-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="0126b-194">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="0126b-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="0126b-195">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0126b-196">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0126b-197">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0126b-198">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0126b-199">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0126b-200">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0126b-201">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0126b-202">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="0126b-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0126b-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0126b-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0126b-204">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="0126b-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="0126b-205">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="0126b-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="0126b-206">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="0126b-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0126b-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0126b-207">AzureRM.Resources</span></span>
* <span data-ttu-id="0126b-208">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="0126b-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="0126b-209">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0126b-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="0126b-210">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0126b-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="0126b-211">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="0126b-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="0126b-212">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0126b-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="0126b-213">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0126b-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0126b-214">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="0126b-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0126b-215">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0126b-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="0126b-216">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0126b-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0126b-217">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="0126b-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0126b-218">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="0126b-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="0126b-219">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="0126b-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="0126b-220">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="0126b-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="0126b-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0126b-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0126b-222">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0126b-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0126b-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0126b-223">AzureRM.Sql</span></span>
* <span data-ttu-id="0126b-224">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0126b-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="0126b-225">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="0126b-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="0126b-226">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0126b-227">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="0126b-227">AzureRM.Profile</span></span>
* <span data-ttu-id="0126b-228">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="0126b-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="0126b-229">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="0126b-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0126b-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0126b-230">Azure.Storage</span></span>
* <span data-ttu-id="0126b-231">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="0126b-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0126b-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0126b-232">AzureRM.Compute</span></span>
* <span data-ttu-id="0126b-233">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="0126b-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="0126b-234">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="0126b-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="0126b-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0126b-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0126b-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0126b-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0126b-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0126b-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="0126b-238">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="0126b-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="0126b-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0126b-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="0126b-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0126b-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="0126b-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0126b-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="0126b-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0126b-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="0126b-243">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0126b-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="0126b-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="0126b-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0126b-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="0126b-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="0126b-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="0126b-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="0126b-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="0126b-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="0126b-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0126b-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="0126b-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0126b-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="0126b-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0126b-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0126b-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="0126b-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="0126b-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0126b-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0126b-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0126b-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="0126b-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="0126b-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="0126b-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0126b-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="0126b-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0126b-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="0126b-259">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="0126b-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0126b-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0126b-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0126b-261">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="0126b-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="0126b-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0126b-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="0126b-263">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="0126b-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="0126b-264">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="0126b-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="0126b-265">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="0126b-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0126b-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0126b-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0126b-267">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="0126b-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="0126b-268">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="0126b-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0126b-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0126b-269">AzureRM.Sql</span></span>
* <span data-ttu-id="0126b-270">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="0126b-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0126b-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0126b-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0126b-272">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0126b-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0126b-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0126b-273">AzureRM.Websites</span></span>
* <span data-ttu-id="0126b-274">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0126b-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="0126b-275">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="0126b-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="0126b-276">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="0126b-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0126b-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0126b-278">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="0126b-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="0126b-279">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0126b-280">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="0126b-280">AzureRM.Profile</span></span>
* <span data-ttu-id="0126b-281">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="0126b-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0126b-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0126b-282">AzureRM.Compute</span></span>
* <span data-ttu-id="0126b-283">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="0126b-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="0126b-284">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="0126b-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="0126b-285">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="0126b-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0126b-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0126b-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0126b-287">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="0126b-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="0126b-288">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="0126b-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="0126b-289">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="0126b-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="0126b-290">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="0126b-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="0126b-291">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="0126b-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="0126b-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0126b-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0126b-293">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="0126b-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="0126b-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0126b-294">AzureRM.Network</span></span>
* <span data-ttu-id="0126b-295">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="0126b-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0126b-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0126b-296">AzureRM.Resources</span></span>
* <span data-ttu-id="0126b-297">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="0126b-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="0126b-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="0126b-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="0126b-299">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="0126b-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="0126b-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0126b-300">AzureRM.Sql</span></span>
* <span data-ttu-id="0126b-301">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="0126b-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="0126b-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0126b-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0126b-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0126b-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0126b-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0126b-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0126b-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0126b-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0126b-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0126b-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0126b-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0126b-307">AzureRM.Websites</span></span>
* <span data-ttu-id="0126b-308">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="0126b-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="0126b-309">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="0126b-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0126b-310">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="0126b-310">AzureRM.Profile</span></span>
* <span data-ttu-id="0126b-311">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="0126b-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0126b-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0126b-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0126b-313">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="0126b-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0126b-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0126b-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0126b-315">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="0126b-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="0126b-316">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0126b-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="0126b-317">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="0126b-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="0126b-318">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="0126b-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="0126b-319">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="0126b-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="0126b-320">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="0126b-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="0126b-321">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="0126b-321">Added support for MSI identity</span></span>
* <span data-ttu-id="0126b-322">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="0126b-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="0126b-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0126b-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="0126b-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0126b-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="0126b-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0126b-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="0126b-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0126b-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0126b-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0126b-327">AzureRM.Batch</span></span>
* <span data-ttu-id="0126b-328">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="0126b-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="0126b-329">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="0126b-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0126b-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0126b-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="0126b-331">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="0126b-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0126b-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0126b-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0126b-333">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0126b-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0126b-334">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0126b-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="0126b-335">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0126b-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="0126b-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0126b-336">AzureRM.Network</span></span>
* <span data-ttu-id="0126b-337">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="0126b-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="0126b-338">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="0126b-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="0126b-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0126b-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="0126b-340">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="0126b-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="0126b-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0126b-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0126b-342">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="0126b-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="0126b-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0126b-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0126b-344">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="0126b-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="0126b-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0126b-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0126b-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0126b-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0126b-347">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="0126b-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0126b-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0126b-348">AzureRM.Sql</span></span>
* <span data-ttu-id="0126b-349">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="0126b-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="0126b-350">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="0126b-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="0126b-351">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="0126b-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="0126b-352">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="0126b-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="0126b-353">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="0126b-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="0126b-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0126b-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0126b-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0126b-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0126b-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0126b-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0126b-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0126b-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0126b-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0126b-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0126b-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0126b-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0126b-360">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="0126b-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>