---
ms.openlocfilehash: ac8513b3eee4adfcaf0be8bf7b4e8d09190811df
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516633"
---
## <a name="240---july-2019"></a><span data-ttu-id="f4ffa-101">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-102">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-103">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="f4ffa-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f4ffa-104">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f4ffa-105">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4ffa-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f4ffa-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-106">Az.Advisor</span></span>
* <span data-ttu-id="f4ffa-107">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f4ffa-108">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f4ffa-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-109">Az.ApiManagement</span></span>
* <span data-ttu-id="f4ffa-110">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f4ffa-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f4ffa-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f4ffa-112">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="f4ffa-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f4ffa-113">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f4ffa-114">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f4ffa-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f4ffa-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f4ffa-116">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="f4ffa-116">Added support for specifiying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-117">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-118">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-119">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-120">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4ffa-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ffa-121">Az.DataFactory</span></span>
* <span data-ttu-id="f4ffa-122">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f4ffa-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f4ffa-123">Az.EventGrid</span></span>
* <span data-ttu-id="f4ffa-124">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4ffa-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-125">Az.IotHub</span></span>
* <span data-ttu-id="f4ffa-126">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-127">Az.Network</span></span>
* <span data-ttu-id="f4ffa-128">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="f4ffa-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f4ffa-129">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f4ffa-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="f4ffa-131">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f4ffa-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f4ffa-132">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f4ffa-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f4ffa-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="f4ffa-134">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f4ffa-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-136">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="f4ffa-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-137">Az.Resources</span></span>
    - <span data-ttu-id="f4ffa-138">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="f4ffa-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f4ffa-139">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="f4ffa-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f4ffa-140">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="f4ffa-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f4ffa-141">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f4ffa-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f4ffa-142">Az.ServiceBus</span></span>
* <span data-ttu-id="f4ffa-143">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-144">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-145">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="f4ffa-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f4ffa-146">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f4ffa-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f4ffa-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f4ffa-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f4ffa-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f4ffa-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f4ffa-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f4ffa-153">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="f4ffa-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-154">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-155">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f4ffa-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f4ffa-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f4ffa-157">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f4ffa-158">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="f4ffa-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f4ffa-159">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f4ffa-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f4ffa-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f4ffa-162">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f4ffa-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f4ffa-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f4ffa-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f4ffa-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f4ffa-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f4ffa-165">Az.StorageSync</span></span>
* <span data-ttu-id="f4ffa-166">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f4ffa-167">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-168">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-169">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="f4ffa-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f4ffa-170">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f4ffa-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f4ffa-171">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="f4ffa-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f4ffa-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f4ffa-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f4ffa-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f4ffa-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-174">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-175">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f4ffa-176">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f4ffa-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f4ffa-177">Az.Dns</span></span>
* <span data-ttu-id="f4ffa-178">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f4ffa-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f4ffa-179">Az.EventGrid</span></span>
* <span data-ttu-id="f4ffa-180">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f4ffa-181">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-181">New cmdlets:</span></span>
    - <span data-ttu-id="f4ffa-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f4ffa-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f4ffa-183">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f4ffa-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f4ffa-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f4ffa-185">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f4ffa-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f4ffa-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f4ffa-187">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f4ffa-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f4ffa-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f4ffa-189">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f4ffa-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f4ffa-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f4ffa-191">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f4ffa-192">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f4ffa-193">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f4ffa-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f4ffa-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f4ffa-195">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="f4ffa-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="f4ffa-196">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f4ffa-197">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f4ffa-198">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="f4ffa-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f4ffa-200">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f4ffa-201">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f4ffa-202">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="f4ffa-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f4ffa-203">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f4ffa-204">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="f4ffa-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f4ffa-205">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f4ffa-206">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f4ffa-207">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="f4ffa-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="f4ffa-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f4ffa-209">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f4ffa-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f4ffa-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f4ffa-211">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f4ffa-212">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f4ffa-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-213">Az.FrontDoor</span></span>
* <span data-ttu-id="f4ffa-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f4ffa-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f4ffa-215">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f4ffa-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f4ffa-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f4ffa-217">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="f4ffa-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-218">Az.Network</span></span>
* <span data-ttu-id="f4ffa-219">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f4ffa-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f4ffa-220">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ffa-220">New cmdlets</span></span>
        - <span data-ttu-id="f4ffa-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f4ffa-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f4ffa-222">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f4ffa-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f4ffa-223">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ffa-223">New cmdlets</span></span> 
        - <span data-ttu-id="f4ffa-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f4ffa-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f4ffa-225">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4ffa-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f4ffa-226">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ffa-226">New cmdlets</span></span> 
        - <span data-ttu-id="f4ffa-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4ffa-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="f4ffa-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4ffa-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f4ffa-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4ffa-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f4ffa-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f4ffa-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f4ffa-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f4ffa-232">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4ffa-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f4ffa-233">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ffa-233">New cmdlets</span></span>
        - <span data-ttu-id="f4ffa-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4ffa-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f4ffa-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4ffa-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f4ffa-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4ffa-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f4ffa-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f4ffa-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f4ffa-238">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f4ffa-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f4ffa-239">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f4ffa-240">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f4ffa-241">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f4ffa-242">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f4ffa-243">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f4ffa-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f4ffa-244">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f4ffa-245">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f4ffa-246">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f4ffa-247">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f4ffa-248">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f4ffa-249">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f4ffa-250">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f4ffa-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f4ffa-251">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f4ffa-252">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f4ffa-253">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="f4ffa-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f4ffa-254">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f4ffa-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f4ffa-255">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f4ffa-256">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f4ffa-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="f4ffa-257">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="f4ffa-258">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f4ffa-259">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f4ffa-260">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f4ffa-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="f4ffa-262">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-263">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-264">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f4ffa-265">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f4ffa-266">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f4ffa-267">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4ffa-269">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-270">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-271">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f4ffa-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f4ffa-272">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f4ffa-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f4ffa-273">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f4ffa-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4ffa-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f4ffa-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4ffa-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f4ffa-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4ffa-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f4ffa-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f4ffa-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f4ffa-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f4ffa-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-279">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-280">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4ffa-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f4ffa-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="f4ffa-282">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="f4ffa-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f4ffa-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-284">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-285">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="f4ffa-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f4ffa-286">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f4ffa-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f4ffa-287">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f4ffa-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4ffa-288">Az.Cdn</span></span>
* <span data-ttu-id="f4ffa-289">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-290">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-291">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f4ffa-292">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f4ffa-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f4ffa-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-293">Az.EventHub</span></span>
* <span data-ttu-id="f4ffa-294">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f4ffa-295">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ffa-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-296">Az.Network</span></span>
* <span data-ttu-id="f4ffa-297">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="f4ffa-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f4ffa-298">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ffa-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f4ffa-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="f4ffa-300">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="f4ffa-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-302">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="f4ffa-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f4ffa-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f4ffa-303">Az.ServiceBus</span></span>
* <span data-ttu-id="f4ffa-304">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ffa-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4ffa-306">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f4ffa-307">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-308">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-309">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f4ffa-310">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f4ffa-311">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f4ffa-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f4ffa-312">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-313">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-314">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f4ffa-315">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f4ffa-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-316">Az.ApiManagement</span></span>
* <span data-ttu-id="f4ffa-317">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f4ffa-318">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f4ffa-319">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f4ffa-320">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f4ffa-321">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f4ffa-322">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f4ffa-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f4ffa-323">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f4ffa-324">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f4ffa-325">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f4ffa-326">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="f4ffa-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f4ffa-327">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f4ffa-328">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="f4ffa-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f4ffa-329">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="f4ffa-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f4ffa-330">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f4ffa-331">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f4ffa-332">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f4ffa-333">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f4ffa-334">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="f4ffa-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f4ffa-335">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="f4ffa-336">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="f4ffa-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f4ffa-337">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="f4ffa-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f4ffa-338">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f4ffa-339">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f4ffa-340">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="f4ffa-341">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f4ffa-342">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f4ffa-343">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f4ffa-344">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f4ffa-345">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f4ffa-346">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f4ffa-347">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="f4ffa-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f4ffa-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f4ffa-349">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f4ffa-350">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f4ffa-351">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f4ffa-352">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="f4ffa-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f4ffa-353">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f4ffa-354">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f4ffa-355">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f4ffa-356">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="f4ffa-357">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f4ffa-358">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f4ffa-359">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f4ffa-360">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f4ffa-361">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f4ffa-362">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f4ffa-363">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="f4ffa-364">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f4ffa-365">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f4ffa-366">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f4ffa-367">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f4ffa-368">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f4ffa-369">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f4ffa-370">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f4ffa-371">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f4ffa-372">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f4ffa-373">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f4ffa-374">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f4ffa-375">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f4ffa-376">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f4ffa-377">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f4ffa-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f4ffa-378">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f4ffa-379">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f4ffa-380">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f4ffa-381">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f4ffa-382">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f4ffa-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f4ffa-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f4ffa-384">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f4ffa-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f4ffa-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f4ffa-386">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f4ffa-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f4ffa-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f4ffa-388">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f4ffa-389">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f4ffa-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f4ffa-391">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="f4ffa-392">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f4ffa-393">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-394">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-395">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f4ffa-396">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f4ffa-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f4ffa-397">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f4ffa-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f4ffa-398">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f4ffa-399">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f4ffa-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f4ffa-400">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f4ffa-401">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-402">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-403">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f4ffa-404">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-406">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f4ffa-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-407">Az.Monitor</span></span>
* <span data-ttu-id="f4ffa-408">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="f4ffa-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-409">Az.Network</span></span>
* <span data-ttu-id="f4ffa-410">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f4ffa-411">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="f4ffa-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4ffa-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f4ffa-413">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f4ffa-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-414">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-415">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="f4ffa-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-416">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-417">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="f4ffa-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f4ffa-418">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-419">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-420">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="f4ffa-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4ffa-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4ffa-422">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f4ffa-423">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-424">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-425">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f4ffa-426">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f4ffa-427">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f4ffa-428">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f4ffa-429">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f4ffa-430">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ffa-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f4ffa-431">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="f4ffa-431">Breaking changes</span></span>
    - <span data-ttu-id="f4ffa-432">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f4ffa-433">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f4ffa-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f4ffa-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="f4ffa-435">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f4ffa-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f4ffa-436">Az.Dns</span></span>
* <span data-ttu-id="f4ffa-437">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="f4ffa-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f4ffa-438">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f4ffa-439">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f4ffa-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-440">Az.FrontDoor</span></span>
* <span data-ttu-id="f4ffa-441">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f4ffa-442">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f4ffa-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f4ffa-443">Az.HDInsight</span></span>
* <span data-ttu-id="f4ffa-444">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f4ffa-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f4ffa-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f4ffa-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f4ffa-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f4ffa-447">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f4ffa-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f4ffa-448">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f4ffa-449">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f4ffa-450">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f4ffa-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-451">Az.Monitor</span></span>
* <span data-ttu-id="f4ffa-452">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f4ffa-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f4ffa-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f4ffa-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f4ffa-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f4ffa-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f4ffa-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f4ffa-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f4ffa-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f4ffa-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f4ffa-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f4ffa-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f4ffa-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f4ffa-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f4ffa-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f4ffa-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f4ffa-464">[Mais](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="f4ffa-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f4ffa-465">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-466">Az.Network</span></span>
* <span data-ttu-id="f4ffa-467">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="f4ffa-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f4ffa-468">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ffa-468">New cmdlets</span></span>
        - <span data-ttu-id="f4ffa-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="f4ffa-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f4ffa-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f4ffa-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f4ffa-473">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-473">Updated cmdlets</span></span>
        - <span data-ttu-id="f4ffa-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f4ffa-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f4ffa-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f4ffa-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f4ffa-476">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f4ffa-477">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f4ffa-478">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f4ffa-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="f4ffa-480">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f4ffa-481">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f4ffa-482">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-484">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f4ffa-485">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f4ffa-486">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f4ffa-487">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f4ffa-488">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f4ffa-489">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f4ffa-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f4ffa-490">Az.Relay</span></span>
* <span data-ttu-id="f4ffa-491">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="f4ffa-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f4ffa-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f4ffa-492">Az.ServiceBus</span></span>
* <span data-ttu-id="f4ffa-493">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="f4ffa-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-494">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-495">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="f4ffa-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f4ffa-496">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f4ffa-497">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f4ffa-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="f4ffa-499">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f4ffa-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f4ffa-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f4ffa-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-503">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-504">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f4ffa-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f4ffa-505">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f4ffa-506">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f4ffa-507">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f4ffa-507">Highlights since the last major release</span></span>
* <span data-ttu-id="f4ffa-508">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-508">General availability of `Az` module</span></span>
* <span data-ttu-id="f4ffa-509">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f4ffa-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f4ffa-510">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f4ffa-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f4ffa-511">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f4ffa-512">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f4ffa-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f4ffa-513">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f4ffa-514">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f4ffa-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-515">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-516">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="f4ffa-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f4ffa-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f4ffa-517">Az.Batch</span></span>
* <span data-ttu-id="f4ffa-518">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f4ffa-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4ffa-519">Az.Cdn</span></span>
* <span data-ttu-id="f4ffa-520">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4ffa-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4ffa-522">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-523">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-524">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f4ffa-525">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-526">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f4ffa-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4ffa-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ffa-527">Az.DataFactory</span></span>
* <span data-ttu-id="f4ffa-528">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-530">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f4ffa-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f4ffa-531">Az.EventGrid</span></span>
* <span data-ttu-id="f4ffa-532">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f4ffa-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-533">Az.EventHub</span></span>
* <span data-ttu-id="f4ffa-534">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="f4ffa-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f4ffa-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f4ffa-535">Az.HDInsight</span></span>
* <span data-ttu-id="f4ffa-536">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4ffa-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-537">Az.IotHub</span></span>
* <span data-ttu-id="f4ffa-538">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f4ffa-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-539">Az.KeyVault</span></span>
* <span data-ttu-id="f4ffa-540">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-541">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f4ffa-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f4ffa-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f4ffa-542">Az.MachineLearning</span></span>
* <span data-ttu-id="f4ffa-543">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f4ffa-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f4ffa-544">Az.Media</span></span>
* <span data-ttu-id="f4ffa-545">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f4ffa-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-546">Az.Monitor</span></span>
  * <span data-ttu-id="f4ffa-547">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f4ffa-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f4ffa-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f4ffa-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f4ffa-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f4ffa-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f4ffa-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f4ffa-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f4ffa-553">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f4ffa-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-554">Az.Network</span></span>
* <span data-ttu-id="f4ffa-555">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-556">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f4ffa-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f4ffa-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f4ffa-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="f4ffa-558">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f4ffa-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="f4ffa-560">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f4ffa-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f4ffa-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f4ffa-562">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-564">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-565">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f4ffa-566">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f4ffa-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f4ffa-567">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="f4ffa-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f4ffa-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f4ffa-568">Az.RedisCache</span></span>
* <span data-ttu-id="f4ffa-569">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-570">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-571">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f4ffa-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-572">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-573">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="f4ffa-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f4ffa-574">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-575">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f4ffa-576">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f4ffa-577">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f4ffa-578">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f4ffa-579">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f4ffa-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-580">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-581">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="f4ffa-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f4ffa-582">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f4ffa-583">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f4ffa-584">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f4ffa-585">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f4ffa-586">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f4ffa-586">Highlights since the last major release</span></span>
* <span data-ttu-id="f4ffa-587">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-587">General availability of `Az` module</span></span>
* <span data-ttu-id="f4ffa-588">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f4ffa-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f4ffa-589">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f4ffa-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f4ffa-590">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f4ffa-591">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f4ffa-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f4ffa-592">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f4ffa-593">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f4ffa-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-594">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-595">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ffa-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f4ffa-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="f4ffa-597">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="f4ffa-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f4ffa-598">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="f4ffa-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-599">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-600">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f4ffa-601">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f4ffa-602">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-603">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-604">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f4ffa-605">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f4ffa-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="f4ffa-607">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="f4ffa-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4ffa-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ffa-608">Az.DataFactory</span></span>
* <span data-ttu-id="f4ffa-609">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f4ffa-610">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-611">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-612">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f4ffa-613">Melhorar o tratamento de erros para “Test-AzDeployment” e “Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-613">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f4ffa-614">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="f4ffa-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f4ffa-615">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f4ffa-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f4ffa-616">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="f4ffa-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f4ffa-617">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f4ffa-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-618">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-619">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-620">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-621">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f4ffa-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f4ffa-622">New-AzStorageContext</span></span>
* <span data-ttu-id="f4ffa-623">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f4ffa-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f4ffa-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f4ffa-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f4ffa-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f4ffa-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f4ffa-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f4ffa-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f4ffa-628">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f4ffa-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f4ffa-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f4ffa-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f4ffa-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f4ffa-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f4ffa-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f4ffa-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f4ffa-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f4ffa-633">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f4ffa-634">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f4ffa-634">Highlights since the last major release</span></span>
* <span data-ttu-id="f4ffa-635">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-635">General availability of `Az` module</span></span>
* <span data-ttu-id="f4ffa-636">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f4ffa-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f4ffa-637">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f4ffa-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f4ffa-638">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f4ffa-639">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f4ffa-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f4ffa-640">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f4ffa-641">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f4ffa-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-642">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-643">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f4ffa-644">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="f4ffa-644">Dynamic grouping</span></span>
    * <span data-ttu-id="f4ffa-645">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="f4ffa-645">Pre-Post script</span></span>
    * <span data-ttu-id="f4ffa-646">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="f4ffa-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-647">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-648">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f4ffa-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f4ffa-649">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f4ffa-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-650">Az.KeyVault</span></span>
* <span data-ttu-id="f4ffa-651">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-652">Az.Network</span></span>
* <span data-ttu-id="f4ffa-653">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f4ffa-654">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-656">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f4ffa-657">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="f4ffa-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-658">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-659">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f4ffa-660">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="f4ffa-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-661">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-662">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-663">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-664">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4ffa-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f4ffa-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f4ffa-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f4ffa-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f4ffa-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f4ffa-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f4ffa-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f4ffa-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f4ffa-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-671">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-672">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f4ffa-673">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-674">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-675">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="f4ffa-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f4ffa-676">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-677">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-678">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f4ffa-679">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f4ffa-680">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="f4ffa-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f4ffa-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4ffa-681">Az.Cdn</span></span>
* <span data-ttu-id="f4ffa-682">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-683">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-684">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="f4ffa-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4ffa-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ffa-685">Az.DataFactory</span></span>
* <span data-ttu-id="f4ffa-686">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f4ffa-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4ffa-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4ffa-687">Az.LogicApp</span></span>
* <span data-ttu-id="f4ffa-688">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-689">Az.Network</span></span>
* <span data-ttu-id="f4ffa-690">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-692">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f4ffa-693">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="f4ffa-693">SDK Update</span></span>
* <span data-ttu-id="f4ffa-694">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4ffa-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f4ffa-695">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4ffa-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-696">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-697">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="f4ffa-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f4ffa-698">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f4ffa-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f4ffa-699">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f4ffa-700">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f4ffa-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f4ffa-701">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f4ffa-702">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f4ffa-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-703">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-704">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f4ffa-705">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-706">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-707">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f4ffa-708">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f4ffa-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="f4ffa-710">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-711">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-712">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f4ffa-713">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f4ffa-714">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4ffa-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4ffa-716">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-717">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-718">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="f4ffa-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f4ffa-719">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="f4ffa-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f4ffa-720">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f4ffa-721">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-723">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f4ffa-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-724">Az.EventHub</span></span>
* <span data-ttu-id="f4ffa-725">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f4ffa-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-726">Az.KeyVault</span></span>
* <span data-ttu-id="f4ffa-727">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4ffa-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4ffa-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4ffa-728">Az.LogicApp</span></span>
* <span data-ttu-id="f4ffa-729">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="f4ffa-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f4ffa-730">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="f4ffa-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f4ffa-731">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f4ffa-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f4ffa-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4ffa-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4ffa-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4ffa-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4ffa-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4ffa-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f4ffa-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f4ffa-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f4ffa-736">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="f4ffa-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f4ffa-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4ffa-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4ffa-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f4ffa-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f4ffa-741">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f4ffa-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f4ffa-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-742">Az.Monitor</span></span>
* <span data-ttu-id="f4ffa-743">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-744">Az.Network</span></span>
* <span data-ttu-id="f4ffa-745">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4ffa-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f4ffa-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="f4ffa-747">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f4ffa-748">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f4ffa-749">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f4ffa-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-750">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-751">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f4ffa-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f4ffa-752">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f4ffa-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f4ffa-753">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f4ffa-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f4ffa-754">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="f4ffa-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-755">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-756">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f4ffa-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f4ffa-757">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="f4ffa-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-758">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-759">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f4ffa-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f4ffa-760">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-761">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-762">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4ffa-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f4ffa-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-763">Az.AnalysisServices</span></span>
<span data-ttu-id="f4ffa-764">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-765">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-766">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="f4ffa-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f4ffa-767">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f4ffa-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f4ffa-768">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-769">Az.RecoveryServices</span></span>
<span data-ttu-id="f4ffa-770">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-771">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-772">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f4ffa-773">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f4ffa-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f4ffa-774">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f4ffa-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f4ffa-775">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f4ffa-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-776">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-777">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f4ffa-778">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="f4ffa-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f4ffa-779">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f4ffa-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f4ffa-780">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-781">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-782">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="f4ffa-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f4ffa-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="f4ffa-784">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="f4ffa-786">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f4ffa-787">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-788">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-789">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f4ffa-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f4ffa-790">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4ffa-791">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f4ffa-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f4ffa-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f4ffa-792">Az.Aks</span></span>
* <span data-ttu-id="f4ffa-793">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f4ffa-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-794">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-795">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f4ffa-796">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f4ffa-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f4ffa-797">Az.Cdn</span></span>
* <span data-ttu-id="f4ffa-798">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-799">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-800">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f4ffa-801">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f4ffa-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f4ffa-802">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f4ffa-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f4ffa-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f4ffa-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f4ffa-804">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f4ffa-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4ffa-805">Az.DataFactory</span></span>
* <span data-ttu-id="f4ffa-806">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f4ffa-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-808">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="f4ffa-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f4ffa-809">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f4ffa-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f4ffa-810">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4ffa-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-811">Az.IotHub</span></span>
* <span data-ttu-id="f4ffa-812">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f4ffa-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-813">Az.KeyVault</span></span>
* <span data-ttu-id="f4ffa-814">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-815">Az.Network</span></span>
* <span data-ttu-id="f4ffa-816">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-817">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-818">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f4ffa-819">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f4ffa-820">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f4ffa-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f4ffa-821">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f4ffa-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f4ffa-822">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f4ffa-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f4ffa-823">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f4ffa-824">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f4ffa-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4ffa-826">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f4ffa-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f4ffa-827">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-827">Fix some error messages.</span></span>
* <span data-ttu-id="f4ffa-828">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f4ffa-829">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f4ffa-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f4ffa-830">Az.SignalR</span></span>
* <span data-ttu-id="f4ffa-831">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-832">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-833">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4ffa-834">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f4ffa-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f4ffa-835">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="f4ffa-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f4ffa-836">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-837">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-838">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4ffa-839">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f4ffa-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f4ffa-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f4ffa-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f4ffa-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f4ffa-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f4ffa-842">Az.TrafficManager</span></span>
* <span data-ttu-id="f4ffa-843">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-844">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-845">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f4ffa-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f4ffa-846">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f4ffa-847">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f4ffa-848">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f4ffa-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f4ffa-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-849">Az.Accounts</span></span>
* <span data-ttu-id="f4ffa-850">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f4ffa-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-851">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-852">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f4ffa-853">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="f4ffa-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f4ffa-854">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-856">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f4ffa-857">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="f4ffa-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f4ffa-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f4ffa-858">Az.EventGrid</span></span>
* <span data-ttu-id="f4ffa-859">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f4ffa-860">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f4ffa-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f4ffa-861">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f4ffa-862">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="f4ffa-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f4ffa-863">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f4ffa-864">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f4ffa-865">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f4ffa-866">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="f4ffa-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f4ffa-867">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f4ffa-868">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="f4ffa-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="f4ffa-869">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f4ffa-870">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f4ffa-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-871">Az.IotHub</span></span>
* <span data-ttu-id="f4ffa-872">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="f4ffa-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f4ffa-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f4ffa-873">Az.LogicApp</span></span>
* <span data-ttu-id="f4ffa-874">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="f4ffa-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-875">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-876">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f4ffa-877">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f4ffa-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f4ffa-878">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ffa-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f4ffa-879">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f4ffa-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f4ffa-880">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f4ffa-881">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f4ffa-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f4ffa-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f4ffa-882">Az.SignalR</span></span>
* <span data-ttu-id="f4ffa-883">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-884">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-885">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f4ffa-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-886">Az.Storage</span></span>
* <span data-ttu-id="f4ffa-887">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="f4ffa-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f4ffa-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f4ffa-888">New-AzStorageContext</span></span>
* <span data-ttu-id="f4ffa-889">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f4ffa-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f4ffa-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-891">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-892">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="f4ffa-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f4ffa-893">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f4ffa-894">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f4ffa-895">Geral</span><span class="sxs-lookup"><span data-stu-id="f4ffa-895">General</span></span>

- <span data-ttu-id="f4ffa-896">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="f4ffa-896">General Availability of Az Module</span></span>
- <span data-ttu-id="f4ffa-897">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-897">Online help for each module</span></span>
- <span data-ttu-id="f4ffa-898">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f4ffa-899">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="f4ffa-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f4ffa-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-900">Az.Accounts</span></span>
- <span data-ttu-id="f4ffa-901">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="f4ffa-902">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="f4ffa-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f4ffa-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-903">Az.ApiManagement</span></span>
- <span data-ttu-id="f4ffa-904">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="f4ffa-904">Fixes for #7002</span></span>
- <span data-ttu-id="f4ffa-905">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f4ffa-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f4ffa-906">Az.Batch</span></span>
- <span data-ttu-id="f4ffa-907">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f4ffa-908">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f4ffa-909">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f4ffa-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4ffa-910">Az.Billing</span></span>
- <span data-ttu-id="f4ffa-911">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f4ffa-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-912">Az.CognitivServices</span></span>
- <span data-ttu-id="f4ffa-913">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f4ffa-914">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f4ffa-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f4ffa-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="f4ffa-916">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f4ffa-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f4ffa-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f4ffa-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f4ffa-918">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="f4ffa-920">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f4ffa-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-921">Az.Monitor</span></span>
- <span data-ttu-id="f4ffa-922">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f4ffa-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f4ffa-923">Az.KeyVault</span></span>
- <span data-ttu-id="f4ffa-924">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="f4ffa-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f4ffa-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f4ffa-925">Az.MachineLearning</span></span>
- <span data-ttu-id="f4ffa-926">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f4ffa-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f4ffa-927">Az.Media</span></span>
- <span data-ttu-id="f4ffa-928">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f4ffa-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f4ffa-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-929">Az.Network</span></span>
<span data-ttu-id="f4ffa-930">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f4ffa-931">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f4ffa-931">New cmdlets added:</span></span>
        - <span data-ttu-id="f4ffa-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f4ffa-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f4ffa-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ffa-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f4ffa-940">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f4ffa-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4ffa-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f4ffa-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f4ffa-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f4ffa-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f4ffa-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f4ffa-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f4ffa-946">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f4ffa-947">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f4ffa-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f4ffa-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4ffa-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f4ffa-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4ffa-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f4ffa-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f4ffa-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f4ffa-951">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f4ffa-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f4ffa-952">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f4ffa-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="f4ffa-954">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f4ffa-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-955">Az.Profile</span></span>
- <span data-ttu-id="f4ffa-956">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4ffa-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="f4ffa-958">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f4ffa-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-959">Az.Resources</span></span>
- <span data-ttu-id="f4ffa-960">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="f4ffa-962">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="f4ffa-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f4ffa-963">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f4ffa-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f4ffa-964">Az.SIgnalR</span></span>
- <span data-ttu-id="f4ffa-965">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f4ffa-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f4ffa-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-966">Az.Sql</span></span>
- <span data-ttu-id="f4ffa-967">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="f4ffa-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f4ffa-968">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="f4ffa-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f4ffa-969">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f4ffa-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-970">Az.Storage</span></span>
- <span data-ttu-id="f4ffa-971">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f4ffa-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-972">Az.Websites</span></span>
- <span data-ttu-id="f4ffa-973">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f4ffa-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f4ffa-974">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f4ffa-975">Geral</span><span class="sxs-lookup"><span data-stu-id="f4ffa-975">General</span></span>

* <span data-ttu-id="f4ffa-976">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="f4ffa-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f4ffa-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-977">Az.Compute</span></span>

* <span data-ttu-id="f4ffa-978">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="f4ffa-980">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="f4ffa-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f4ffa-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f4ffa-981">Az.FrontDoor</span></span>

* <span data-ttu-id="f4ffa-982">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="f4ffa-982">Fixed some broken links</span></span>
    - <span data-ttu-id="f4ffa-983">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f4ffa-984">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f4ffa-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="f4ffa-986">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f4ffa-987">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f4ffa-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-988">Az.Resources</span></span>

* <span data-ttu-id="f4ffa-989">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f4ffa-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f4ffa-990">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f4ffa-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-991">Az.Sql</span></span>

* <span data-ttu-id="f4ffa-992">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="f4ffa-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f4ffa-993">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="f4ffa-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f4ffa-994">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f4ffa-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-995">Az.Storage</span></span>

* <span data-ttu-id="f4ffa-996">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f4ffa-997">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="f4ffa-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f4ffa-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f4ffa-999">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="f4ffa-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="f4ffa-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f4ffa-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f4ffa-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1002">Az.Websites</span></span>

* <span data-ttu-id="f4ffa-1003">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f4ffa-1004">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f4ffa-1005">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f4ffa-1006">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f4ffa-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="f4ffa-1008">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f4ffa-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1009">Az.Automation</span></span>
* <span data-ttu-id="f4ffa-1010">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f4ffa-1011">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f4ffa-1012">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f4ffa-1013">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f4ffa-1014">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f4ffa-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1015">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-1016">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f4ffa-1017">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f4ffa-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="f4ffa-1019">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f4ffa-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f4ffa-1021">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f4ffa-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1022">Az.Network</span></span>
* <span data-ttu-id="f4ffa-1023">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f4ffa-1024">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f4ffa-1025">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f4ffa-1026">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f4ffa-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f4ffa-1028">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f4ffa-1029">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f4ffa-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f4ffa-1031">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f4ffa-1032">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f4ffa-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1033">Az.Relay</span></span>
* <span data-ttu-id="f4ffa-1034">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f4ffa-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1035">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-1036">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f4ffa-1037">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f4ffa-1038">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4ffa-1040">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f4ffa-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1041">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-1042">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f4ffa-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4ffa-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4ffa-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4ffa-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f4ffa-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4ffa-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4ffa-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f4ffa-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f4ffa-1051">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f4ffa-1052">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f4ffa-1053">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f4ffa-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f4ffa-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f4ffa-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f4ffa-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f4ffa-1058">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f4ffa-1059">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f4ffa-1060">Geral</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1060">General</span></span>
* <span data-ttu-id="f4ffa-1061">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f4ffa-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1062">Az.Profile</span></span>
* <span data-ttu-id="f4ffa-1063">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f4ffa-1064">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f4ffa-1065">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f4ffa-1066">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f4ffa-1067">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f4ffa-1068">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f4ffa-1069">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f4ffa-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4ffa-1071">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1072">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-1073">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f4ffa-1074">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f4ffa-1075">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-1077">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f4ffa-1078">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f4ffa-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1079">Az.Insights</span></span>
* <span data-ttu-id="f4ffa-1080">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f4ffa-1081">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f4ffa-1082">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f4ffa-1083">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1084">Az.Network</span></span>
* <span data-ttu-id="f4ffa-1085">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f4ffa-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f4ffa-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f4ffa-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f4ffa-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f4ffa-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f4ffa-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f4ffa-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="f4ffa-1093">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1094">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-1095">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f4ffa-1096">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f4ffa-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="f4ffa-1098">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f4ffa-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="f4ffa-1100">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f4ffa-1101">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f4ffa-1102">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f4ffa-1103">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f4ffa-1104">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f4ffa-1105">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f4ffa-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1106">Az.Profile</span></span>
* <span data-ttu-id="f4ffa-1107">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f4ffa-1108">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1109">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-1110">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f4ffa-1111">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f4ffa-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="f4ffa-1113">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f4ffa-1114">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f4ffa-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f4ffa-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f4ffa-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1118">Az.Network</span></span>
* <span data-ttu-id="f4ffa-1119">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f4ffa-1120">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1121">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-1122">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f4ffa-1123">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f4ffa-1124">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f4ffa-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1125">Azure.Storage</span></span>
* <span data-ttu-id="f4ffa-1126">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f4ffa-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f4ffa-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f4ffa-1129">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f4ffa-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f4ffa-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="f4ffa-1132">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f4ffa-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1133">Az.Compute</span></span>
* <span data-ttu-id="f4ffa-1134">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f4ffa-1135">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f4ffa-1136">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f4ffa-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f4ffa-1138">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f4ffa-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1139">Az.Network</span></span>
* <span data-ttu-id="f4ffa-1140">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f4ffa-1141">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1141">new cmdlets added</span></span>
    - <span data-ttu-id="f4ffa-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4ffa-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4ffa-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4ffa-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f4ffa-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f4ffa-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f4ffa-1148">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f4ffa-1149">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f4ffa-1150">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f4ffa-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1151">Az.RedisCache</span></span>
* <span data-ttu-id="f4ffa-1152">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f4ffa-1153">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f4ffa-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1154">Az.Resources</span></span>
* <span data-ttu-id="f4ffa-1155">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f4ffa-1156">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f4ffa-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1157">Az.Sql</span></span>
* <span data-ttu-id="f4ffa-1158">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f4ffa-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1159">Az.Websites</span></span>
* <span data-ttu-id="f4ffa-1160">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f4ffa-1161">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f4ffa-1162">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f4ffa-1163">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="f4ffa-1163">Initial Release</span></span>