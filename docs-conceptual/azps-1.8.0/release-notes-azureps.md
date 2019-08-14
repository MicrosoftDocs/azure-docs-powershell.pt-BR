---
ms.openlocfilehash: faf9313d642a3ca45731f4527aafdfd7f5096a78
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861280"
---
## <a name="180---april-2019"></a><span data-ttu-id="822e3-101">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="822e3-102">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="822e3-102">Highlights since the last major release</span></span>
* <span data-ttu-id="822e3-103">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="822e3-103">General availability of `Az` module</span></span>
* <span data-ttu-id="822e3-104">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="822e3-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="822e3-105">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="822e3-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="822e3-106">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="822e3-107">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="822e3-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="822e3-108">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="822e3-109">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="822e3-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="822e3-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-110">Az.Accounts</span></span>
* <span data-ttu-id="822e3-111">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="822e3-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="822e3-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="822e3-112">Az.Batch</span></span>
* <span data-ttu-id="822e3-113">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="822e3-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="822e3-114">Az.Cdn</span></span>
* <span data-ttu-id="822e3-115">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="822e3-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="822e3-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="822e3-117">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-118">Az.Compute</span></span>
* <span data-ttu-id="822e3-119">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="822e3-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="822e3-120">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-121">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="822e3-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="822e3-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="822e3-122">Az.DataFactory</span></span>
* <span data-ttu-id="822e3-123">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="822e3-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-125">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="822e3-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="822e3-126">Az.EventGrid</span></span>
* <span data-ttu-id="822e3-127">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="822e3-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="822e3-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="822e3-128">Az.EventHub</span></span>
* <span data-ttu-id="822e3-129">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="822e3-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="822e3-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="822e3-130">Az.HDInsight</span></span>
* <span data-ttu-id="822e3-131">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="822e3-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="822e3-132">Az.IotHub</span></span>
* <span data-ttu-id="822e3-133">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="822e3-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-134">Az.KeyVault</span></span>
* <span data-ttu-id="822e3-135">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-136">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="822e3-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="822e3-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="822e3-137">Az.MachineLearning</span></span>
* <span data-ttu-id="822e3-138">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="822e3-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="822e3-139">Az.Media</span></span>
* <span data-ttu-id="822e3-140">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="822e3-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="822e3-141">Az.Monitor</span></span>
  * <span data-ttu-id="822e3-142">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="822e3-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="822e3-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="822e3-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="822e3-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="822e3-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="822e3-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="822e3-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="822e3-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="822e3-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="822e3-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="822e3-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="822e3-148">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="822e3-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-149">Az.Network</span></span>
* <span data-ttu-id="822e3-150">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-151">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="822e3-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="822e3-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="822e3-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="822e3-153">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="822e3-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="822e3-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="822e3-155">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="822e3-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="822e3-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="822e3-157">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="822e3-159">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-160">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="822e3-161">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="822e3-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="822e3-162">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="822e3-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="822e3-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="822e3-163">Az.RedisCache</span></span>
* <span data-ttu-id="822e3-164">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-165">Az.Resources</span></span>
* <span data-ttu-id="822e3-166">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="822e3-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-167">Az.Sql</span></span>
* <span data-ttu-id="822e3-168">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="822e3-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="822e3-169">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-170">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="822e3-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="822e3-171">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="822e3-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="822e3-172">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="822e3-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="822e3-173">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="822e3-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="822e3-174">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="822e3-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-175">Az.Websites</span></span>
* <span data-ttu-id="822e3-176">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="822e3-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="822e3-177">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="822e3-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="822e3-178">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="822e3-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="822e3-179">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="822e3-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="822e3-180">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="822e3-181">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="822e3-181">Highlights since the last major release</span></span>
* <span data-ttu-id="822e3-182">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="822e3-182">General availability of `Az` module</span></span>
* <span data-ttu-id="822e3-183">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="822e3-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="822e3-184">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="822e3-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="822e3-185">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="822e3-186">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="822e3-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="822e3-187">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="822e3-188">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="822e3-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="822e3-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-189">Az.Accounts</span></span>
* <span data-ttu-id="822e3-190">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="822e3-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="822e3-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="822e3-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="822e3-192">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="822e3-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="822e3-193">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="822e3-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="822e3-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-194">Az.Automation</span></span>
* <span data-ttu-id="822e3-195">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="822e3-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="822e3-196">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="822e3-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="822e3-197">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-198">Az.Compute</span></span>
* <span data-ttu-id="822e3-199">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="822e3-200">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="822e3-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="822e3-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="822e3-202">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="822e3-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="822e3-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="822e3-203">Az.DataFactory</span></span>
* <span data-ttu-id="822e3-204">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="822e3-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="822e3-205">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="822e3-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-206">Az.Resources</span></span>
* <span data-ttu-id="822e3-207">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="822e3-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="822e3-208">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="822e3-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="822e3-209">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="822e3-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="822e3-210">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="822e3-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="822e3-211">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="822e3-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="822e3-212">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="822e3-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-213">Az.Sql</span></span>
* <span data-ttu-id="822e3-214">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="822e3-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="822e3-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-215">Az.Storage</span></span>
* <span data-ttu-id="822e3-216">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="822e3-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="822e3-217">New-AzStorageContext</span></span>
* <span data-ttu-id="822e3-218">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="822e3-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="822e3-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="822e3-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="822e3-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="822e3-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="822e3-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="822e3-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="822e3-223">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="822e3-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="822e3-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="822e3-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="822e3-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="822e3-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="822e3-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="822e3-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="822e3-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="822e3-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="822e3-228">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="822e3-229">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="822e3-229">Highlights since the last major release</span></span>
* <span data-ttu-id="822e3-230">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="822e3-230">General availability of `Az` module</span></span>
* <span data-ttu-id="822e3-231">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="822e3-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="822e3-232">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="822e3-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="822e3-233">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="822e3-234">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="822e3-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="822e3-235">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="822e3-236">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="822e3-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="822e3-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-237">Az.Automation</span></span>
* <span data-ttu-id="822e3-238">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="822e3-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="822e3-239">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="822e3-239">Dynamic grouping</span></span>
    * <span data-ttu-id="822e3-240">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="822e3-240">Pre-Post script</span></span>
    * <span data-ttu-id="822e3-241">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="822e3-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-242">Az.Compute</span></span>
* <span data-ttu-id="822e3-243">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="822e3-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="822e3-244">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="822e3-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="822e3-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-245">Az.KeyVault</span></span>
* <span data-ttu-id="822e3-246">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-247">Az.Network</span></span>
* <span data-ttu-id="822e3-248">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="822e3-249">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="822e3-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="822e3-251">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="822e3-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="822e3-252">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="822e3-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-253">Az.Resources</span></span>
* <span data-ttu-id="822e3-254">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="822e3-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="822e3-255">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="822e3-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-256">Az.Sql</span></span>
* <span data-ttu-id="822e3-257">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="822e3-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="822e3-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-258">Az.Storage</span></span>
* <span data-ttu-id="822e3-259">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="822e3-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="822e3-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="822e3-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="822e3-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="822e3-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="822e3-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="822e3-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="822e3-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="822e3-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="822e3-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-266">Az.Websites</span></span>
* <span data-ttu-id="822e3-267">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="822e3-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="822e3-268">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="822e3-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-269">Az.Accounts</span></span>
* <span data-ttu-id="822e3-270">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="822e3-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="822e3-271">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="822e3-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-272">Az.Automation</span></span>
* <span data-ttu-id="822e3-273">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="822e3-274">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="822e3-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="822e3-275">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="822e3-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="822e3-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="822e3-276">Az.Cdn</span></span>
* <span data-ttu-id="822e3-277">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="822e3-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-278">Az.Compute</span></span>
* <span data-ttu-id="822e3-279">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="822e3-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="822e3-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="822e3-280">Az.DataFactory</span></span>
* <span data-ttu-id="822e3-281">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="822e3-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="822e3-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="822e3-282">Az.LogicApp</span></span>
* <span data-ttu-id="822e3-283">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="822e3-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-284">Az.Network</span></span>
* <span data-ttu-id="822e3-285">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="822e3-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="822e3-287">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="822e3-288">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="822e3-288">SDK Update</span></span>
* <span data-ttu-id="822e3-289">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="822e3-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="822e3-290">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="822e3-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-291">Az.Resources</span></span>
* <span data-ttu-id="822e3-292">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="822e3-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="822e3-293">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="822e3-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="822e3-294">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="822e3-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="822e3-295">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="822e3-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="822e3-296">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="822e3-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="822e3-297">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="822e3-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-298">Az.Sql</span></span>
* <span data-ttu-id="822e3-299">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="822e3-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="822e3-300">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="822e3-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="822e3-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-301">Az.Storage</span></span>
* <span data-ttu-id="822e3-302">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="822e3-303">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="822e3-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="822e3-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="822e3-305">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="822e3-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-306">Az.Automation</span></span>
* <span data-ttu-id="822e3-307">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="822e3-308">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="822e3-309">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="822e3-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="822e3-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="822e3-311">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="822e3-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-312">Az.Compute</span></span>
* <span data-ttu-id="822e3-313">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="822e3-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="822e3-314">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="822e3-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="822e3-315">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="822e3-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="822e3-316">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="822e3-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-318">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="822e3-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="822e3-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="822e3-319">Az.EventHub</span></span>
* <span data-ttu-id="822e3-320">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="822e3-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="822e3-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-321">Az.KeyVault</span></span>
* <span data-ttu-id="822e3-322">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="822e3-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="822e3-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="822e3-323">Az.LogicApp</span></span>
* <span data-ttu-id="822e3-324">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="822e3-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="822e3-325">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="822e3-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="822e3-326">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="822e3-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="822e3-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="822e3-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="822e3-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="822e3-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="822e3-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="822e3-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="822e3-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="822e3-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="822e3-331">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="822e3-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="822e3-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="822e3-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="822e3-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="822e3-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="822e3-336">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="822e3-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="822e3-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="822e3-337">Az.Monitor</span></span>
* <span data-ttu-id="822e3-338">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="822e3-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-339">Az.Network</span></span>
* <span data-ttu-id="822e3-340">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="822e3-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="822e3-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="822e3-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="822e3-342">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="822e3-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="822e3-343">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="822e3-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="822e3-344">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="822e3-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="822e3-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-345">Az.Resources</span></span>
* <span data-ttu-id="822e3-346">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="822e3-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="822e3-347">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="822e3-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="822e3-348">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="822e3-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="822e3-349">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="822e3-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-350">Az.Sql</span></span>
* <span data-ttu-id="822e3-351">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="822e3-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="822e3-352">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="822e3-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-353">Az.Websites</span></span>
* <span data-ttu-id="822e3-354">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="822e3-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="822e3-355">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="822e3-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-356">Az.Accounts</span></span>
* <span data-ttu-id="822e3-357">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="822e3-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="822e3-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="822e3-358">Az.AnalysisServices</span></span>
<span data-ttu-id="822e3-359">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="822e3-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-360">Az.Compute</span></span>
* <span data-ttu-id="822e3-361">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="822e3-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="822e3-362">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="822e3-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="822e3-363">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="822e3-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-364">Az.RecoveryServices</span></span>
<span data-ttu-id="822e3-365">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="822e3-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-366">Az.Resources</span></span>
* <span data-ttu-id="822e3-367">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="822e3-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="822e3-368">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="822e3-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="822e3-369">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="822e3-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="822e3-370">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="822e3-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-371">Az.Sql</span></span>
* <span data-ttu-id="822e3-372">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="822e3-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="822e3-373">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="822e3-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="822e3-374">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="822e3-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="822e3-375">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="822e3-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-376">Az.Accounts</span></span>
* <span data-ttu-id="822e3-377">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="822e3-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="822e3-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="822e3-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="822e3-379">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="822e3-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="822e3-381">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="822e3-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="822e3-382">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="822e3-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-383">Az.Accounts</span></span>
* <span data-ttu-id="822e3-384">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="822e3-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="822e3-385">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="822e3-386">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="822e3-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="822e3-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="822e3-387">Az.Aks</span></span>
* <span data-ttu-id="822e3-388">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="822e3-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-389">Az.Automation</span></span>
* <span data-ttu-id="822e3-390">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="822e3-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="822e3-391">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="822e3-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="822e3-392">Az.Cdn</span></span>
* <span data-ttu-id="822e3-393">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-394">Az.Compute</span></span>
* <span data-ttu-id="822e3-395">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="822e3-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="822e3-396">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="822e3-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="822e3-397">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="822e3-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="822e3-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="822e3-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="822e3-399">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="822e3-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="822e3-400">Az.DataFactory</span></span>
* <span data-ttu-id="822e3-401">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="822e3-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-403">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="822e3-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="822e3-404">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="822e3-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="822e3-405">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="822e3-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="822e3-406">Az.IotHub</span></span>
* <span data-ttu-id="822e3-407">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="822e3-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="822e3-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-408">Az.KeyVault</span></span>
* <span data-ttu-id="822e3-409">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-410">Az.Network</span></span>
* <span data-ttu-id="822e3-411">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-412">Az.Resources</span></span>
* <span data-ttu-id="822e3-413">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="822e3-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="822e3-414">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="822e3-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="822e3-415">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="822e3-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="822e3-416">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="822e3-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="822e3-417">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="822e3-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="822e3-418">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="822e3-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="822e3-419">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="822e3-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="822e3-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="822e3-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="822e3-421">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="822e3-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="822e3-422">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="822e3-422">Fix some error messages.</span></span>
* <span data-ttu-id="822e3-423">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="822e3-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="822e3-424">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="822e3-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="822e3-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="822e3-425">Az.SignalR</span></span>
* <span data-ttu-id="822e3-426">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-427">Az.Sql</span></span>
* <span data-ttu-id="822e3-428">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="822e3-429">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="822e3-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="822e3-430">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="822e3-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="822e3-431">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="822e3-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="822e3-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-432">Az.Storage</span></span>
* <span data-ttu-id="822e3-433">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="822e3-434">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="822e3-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="822e3-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="822e3-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="822e3-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="822e3-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="822e3-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="822e3-437">Az.TrafficManager</span></span>
* <span data-ttu-id="822e3-438">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-439">Az.Websites</span></span>
* <span data-ttu-id="822e3-440">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="822e3-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="822e3-441">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="822e3-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="822e3-442">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="822e3-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="822e3-443">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="822e3-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="822e3-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-444">Az.Accounts</span></span>
* <span data-ttu-id="822e3-445">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="822e3-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-446">Az.Compute</span></span>
* <span data-ttu-id="822e3-447">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="822e3-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="822e3-448">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="822e3-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="822e3-449">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-451">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="822e3-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="822e3-452">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="822e3-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="822e3-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="822e3-453">Az.EventGrid</span></span>
* <span data-ttu-id="822e3-454">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="822e3-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="822e3-455">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="822e3-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="822e3-456">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="822e3-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="822e3-457">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="822e3-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="822e3-458">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="822e3-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="822e3-459">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="822e3-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="822e3-460">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="822e3-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="822e3-461">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="822e3-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="822e3-462">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="822e3-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="822e3-463">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="822e3-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="822e3-464">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="822e3-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="822e3-465">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="822e3-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="822e3-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="822e3-466">Az.IotHub</span></span>
* <span data-ttu-id="822e3-467">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="822e3-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="822e3-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="822e3-468">Az.LogicApp</span></span>
* <span data-ttu-id="822e3-469">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="822e3-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-470">Az.Resources</span></span>
* <span data-ttu-id="822e3-471">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="822e3-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="822e3-472">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="822e3-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="822e3-473">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="822e3-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="822e3-474">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="822e3-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="822e3-475">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="822e3-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="822e3-476">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="822e3-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="822e3-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="822e3-477">Az.SignalR</span></span>
* <span data-ttu-id="822e3-478">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-479">Az.Sql</span></span>
* <span data-ttu-id="822e3-480">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="822e3-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="822e3-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-481">Az.Storage</span></span>
* <span data-ttu-id="822e3-482">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="822e3-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="822e3-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="822e3-483">New-AzStorageContext</span></span>
* <span data-ttu-id="822e3-484">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="822e3-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="822e3-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="822e3-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-486">Az.Websites</span></span>
* <span data-ttu-id="822e3-487">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="822e3-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="822e3-488">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="822e3-489">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="822e3-490">Geral</span><span class="sxs-lookup"><span data-stu-id="822e3-490">General</span></span>

- <span data-ttu-id="822e3-491">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="822e3-491">General Availability of Az Module</span></span>
- <span data-ttu-id="822e3-492">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="822e3-492">Online help for each module</span></span>
- <span data-ttu-id="822e3-493">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="822e3-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="822e3-494">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="822e3-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="822e3-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-495">Az.Accounts</span></span>
- <span data-ttu-id="822e3-496">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="822e3-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="822e3-497">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="822e3-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="822e3-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="822e3-498">Az.ApiManagement</span></span>
- <span data-ttu-id="822e3-499">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="822e3-499">Fixes for #7002</span></span>
- <span data-ttu-id="822e3-500">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="822e3-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="822e3-501">Az.Batch</span></span>
- <span data-ttu-id="822e3-502">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="822e3-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="822e3-503">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="822e3-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="822e3-504">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="822e3-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="822e3-505">Az.Billing</span></span>
- <span data-ttu-id="822e3-506">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="822e3-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="822e3-507">Az.CognitivServices</span></span>
- <span data-ttu-id="822e3-508">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="822e3-509">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="822e3-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="822e3-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="822e3-511">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="822e3-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="822e3-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="822e3-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="822e3-513">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="822e3-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="822e3-515">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="822e3-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="822e3-516">Az.Monitor</span></span>
- <span data-ttu-id="822e3-517">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="822e3-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="822e3-518">Az.KeyVault</span></span>
- <span data-ttu-id="822e3-519">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="822e3-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="822e3-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="822e3-520">Az.MachineLearning</span></span>
- <span data-ttu-id="822e3-521">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="822e3-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="822e3-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="822e3-522">Az.Media</span></span>
- <span data-ttu-id="822e3-523">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="822e3-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="822e3-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-524">Az.Network</span></span>
<span data-ttu-id="822e3-525">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="822e3-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="822e3-526">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="822e3-526">New cmdlets added:</span></span>
        - <span data-ttu-id="822e3-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="822e3-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="822e3-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="822e3-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="822e3-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="822e3-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="822e3-535">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="822e3-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="822e3-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="822e3-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="822e3-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="822e3-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="822e3-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="822e3-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="822e3-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="822e3-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="822e3-541">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="822e3-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="822e3-542">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="822e3-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="822e3-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="822e3-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="822e3-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="822e3-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="822e3-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="822e3-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="822e3-546">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="822e3-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="822e3-547">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="822e3-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="822e3-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="822e3-549">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="822e3-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="822e3-550">Az.Profile</span></span>
- <span data-ttu-id="822e3-551">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="822e3-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="822e3-553">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="822e3-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-554">Az.Resources</span></span>
- <span data-ttu-id="822e3-555">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="822e3-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="822e3-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="822e3-557">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="822e3-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="822e3-558">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="822e3-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="822e3-559">Az.SIgnalR</span></span>
- <span data-ttu-id="822e3-560">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="822e3-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="822e3-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-561">Az.Sql</span></span>
- <span data-ttu-id="822e3-562">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="822e3-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="822e3-563">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="822e3-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="822e3-564">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="822e3-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-565">Az.Storage</span></span>
- <span data-ttu-id="822e3-566">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="822e3-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-567">Az.Websites</span></span>
- <span data-ttu-id="822e3-568">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="822e3-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="822e3-569">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="822e3-570">Geral</span><span class="sxs-lookup"><span data-stu-id="822e3-570">General</span></span>

* <span data-ttu-id="822e3-571">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="822e3-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="822e3-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-572">Az.Compute</span></span>

* <span data-ttu-id="822e3-573">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="822e3-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="822e3-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="822e3-575">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="822e3-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="822e3-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="822e3-576">Az.FrontDoor</span></span>

* <span data-ttu-id="822e3-577">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="822e3-577">Fixed some broken links</span></span>
    - <span data-ttu-id="822e3-578">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="822e3-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="822e3-579">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="822e3-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="822e3-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="822e3-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="822e3-581">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="822e3-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="822e3-582">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="822e3-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="822e3-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-583">Az.Resources</span></span>

* <span data-ttu-id="822e3-584">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="822e3-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="822e3-585">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="822e3-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="822e3-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-586">Az.Sql</span></span>

* <span data-ttu-id="822e3-587">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="822e3-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="822e3-588">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="822e3-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="822e3-589">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="822e3-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="822e3-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-590">Az.Storage</span></span>

* <span data-ttu-id="822e3-591">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="822e3-592">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="822e3-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="822e3-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="822e3-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="822e3-594">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="822e3-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="822e3-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="822e3-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="822e3-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="822e3-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="822e3-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-597">Az.Websites</span></span>

* <span data-ttu-id="822e3-598">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="822e3-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="822e3-599">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="822e3-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="822e3-600">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="822e3-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="822e3-601">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="822e3-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="822e3-602">Az.ApiManagement</span></span>
* <span data-ttu-id="822e3-603">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="822e3-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="822e3-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="822e3-604">Az.Automation</span></span>
* <span data-ttu-id="822e3-605">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="822e3-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="822e3-606">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="822e3-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="822e3-607">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="822e3-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="822e3-608">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="822e3-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="822e3-609">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="822e3-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="822e3-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-610">Az.Compute</span></span>
* <span data-ttu-id="822e3-611">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="822e3-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="822e3-612">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="822e3-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="822e3-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="822e3-614">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="822e3-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="822e3-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="822e3-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="822e3-616">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="822e3-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="822e3-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-617">Az.Network</span></span>
* <span data-ttu-id="822e3-618">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="822e3-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="822e3-619">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="822e3-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="822e3-620">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="822e3-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="822e3-621">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="822e3-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="822e3-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="822e3-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="822e3-623">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="822e3-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="822e3-624">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="822e3-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="822e3-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="822e3-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="822e3-626">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="822e3-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="822e3-627">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="822e3-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="822e3-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="822e3-628">Az.Relay</span></span>
* <span data-ttu-id="822e3-629">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="822e3-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="822e3-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-630">Az.Resources</span></span>
* <span data-ttu-id="822e3-631">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="822e3-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="822e3-632">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="822e3-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="822e3-633">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="822e3-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="822e3-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="822e3-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="822e3-635">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="822e3-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="822e3-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-636">Az.Sql</span></span>
* <span data-ttu-id="822e3-637">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="822e3-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="822e3-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="822e3-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="822e3-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="822e3-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="822e3-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="822e3-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="822e3-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="822e3-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="822e3-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="822e3-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="822e3-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="822e3-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="822e3-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="822e3-646">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="822e3-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="822e3-647">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="822e3-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="822e3-648">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="822e3-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="822e3-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="822e3-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="822e3-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="822e3-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="822e3-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="822e3-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="822e3-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="822e3-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="822e3-653">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="822e3-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="822e3-654">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="822e3-655">Geral</span><span class="sxs-lookup"><span data-stu-id="822e3-655">General</span></span>
* <span data-ttu-id="822e3-656">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="822e3-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="822e3-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="822e3-657">Az.Profile</span></span>
* <span data-ttu-id="822e3-658">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="822e3-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="822e3-659">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="822e3-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="822e3-660">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="822e3-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="822e3-661">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="822e3-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="822e3-662">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="822e3-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="822e3-663">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="822e3-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="822e3-664">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="822e3-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="822e3-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="822e3-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="822e3-666">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="822e3-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-667">Az.Compute</span></span>
* <span data-ttu-id="822e3-668">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="822e3-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="822e3-669">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="822e3-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="822e3-670">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="822e3-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-672">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="822e3-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="822e3-673">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="822e3-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="822e3-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="822e3-674">Az.Insights</span></span>
* <span data-ttu-id="822e3-675">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="822e3-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="822e3-676">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="822e3-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="822e3-677">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="822e3-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="822e3-678">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="822e3-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-679">Az.Network</span></span>
* <span data-ttu-id="822e3-680">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="822e3-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="822e3-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="822e3-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="822e3-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="822e3-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="822e3-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="822e3-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="822e3-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="822e3-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="822e3-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="822e3-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="822e3-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="822e3-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="822e3-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="822e3-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="822e3-688">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="822e3-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-689">Az.Resources</span></span>
* <span data-ttu-id="822e3-690">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="822e3-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="822e3-691">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="822e3-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="822e3-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="822e3-692">Az.ServiceBus</span></span>
* <span data-ttu-id="822e3-693">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="822e3-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="822e3-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="822e3-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="822e3-695">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="822e3-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="822e3-696">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="822e3-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="822e3-697">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="822e3-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="822e3-698">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="822e3-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="822e3-699">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="822e3-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="822e3-700">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="822e3-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="822e3-701">Az.Profile</span></span>
* <span data-ttu-id="822e3-702">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="822e3-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="822e3-703">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="822e3-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-704">Az.Compute</span></span>
* <span data-ttu-id="822e3-705">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="822e3-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="822e3-706">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="822e3-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="822e3-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="822e3-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="822e3-708">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="822e3-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="822e3-709">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="822e3-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="822e3-710">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="822e3-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="822e3-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="822e3-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="822e3-712">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="822e3-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-713">Az.Network</span></span>
* <span data-ttu-id="822e3-714">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="822e3-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="822e3-715">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="822e3-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-716">Az.Resources</span></span>
* <span data-ttu-id="822e3-717">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="822e3-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="822e3-718">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="822e3-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="822e3-719">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="822e3-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="822e3-720">Azure.Storage</span></span>
* <span data-ttu-id="822e3-721">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="822e3-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="822e3-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="822e3-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="822e3-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="822e3-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="822e3-724">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="822e3-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="822e3-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="822e3-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="822e3-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="822e3-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="822e3-727">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="822e3-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="822e3-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="822e3-728">Az.Compute</span></span>
* <span data-ttu-id="822e3-729">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="822e3-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="822e3-730">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="822e3-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="822e3-731">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="822e3-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="822e3-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="822e3-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="822e3-733">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="822e3-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="822e3-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="822e3-734">Az.Network</span></span>
* <span data-ttu-id="822e3-735">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="822e3-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="822e3-736">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="822e3-736">new cmdlets added</span></span>
    - <span data-ttu-id="822e3-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="822e3-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="822e3-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="822e3-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="822e3-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="822e3-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="822e3-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="822e3-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="822e3-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="822e3-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="822e3-743">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="822e3-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="822e3-744">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="822e3-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="822e3-745">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="822e3-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="822e3-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="822e3-746">Az.RedisCache</span></span>
* <span data-ttu-id="822e3-747">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="822e3-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="822e3-748">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="822e3-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="822e3-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="822e3-749">Az.Resources</span></span>
* <span data-ttu-id="822e3-750">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="822e3-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="822e3-751">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="822e3-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="822e3-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="822e3-752">Az.Sql</span></span>
* <span data-ttu-id="822e3-753">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="822e3-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="822e3-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="822e3-754">Az.Websites</span></span>
* <span data-ttu-id="822e3-755">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="822e3-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="822e3-756">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="822e3-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="822e3-757">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="822e3-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="822e3-758">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="822e3-758">Initial Release</span></span>