---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 34b21292ccc47bb53b6609cd637ef18338a45cd3
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121469"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="994c5-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="994c5-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="994c5-104">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="994c5-105">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="994c5-105">Highlights since the last major release</span></span>
* <span data-ttu-id="994c5-106">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="994c5-106">General availability of `Az` module</span></span>
* <span data-ttu-id="994c5-107">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="994c5-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="994c5-108">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="994c5-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="994c5-109">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="994c5-110">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="994c5-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="994c5-111">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="994c5-112">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="994c5-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="994c5-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-113">Az.Accounts</span></span>
* <span data-ttu-id="994c5-114">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="994c5-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="994c5-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="994c5-115">Az.Batch</span></span>
* <span data-ttu-id="994c5-116">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="994c5-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="994c5-117">Az.Cdn</span></span>
* <span data-ttu-id="994c5-118">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="994c5-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="994c5-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="994c5-120">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-121">Az.Compute</span></span>
* <span data-ttu-id="994c5-122">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="994c5-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="994c5-123">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-124">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="994c5-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="994c5-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="994c5-125">Az.DataFactory</span></span>
* <span data-ttu-id="994c5-126">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="994c5-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-128">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="994c5-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="994c5-129">Az.EventGrid</span></span>
* <span data-ttu-id="994c5-130">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="994c5-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="994c5-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="994c5-131">Az.EventHub</span></span>
* <span data-ttu-id="994c5-132">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="994c5-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="994c5-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="994c5-133">Az.HDInsight</span></span>
* <span data-ttu-id="994c5-134">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="994c5-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="994c5-135">Az.IotHub</span></span>
* <span data-ttu-id="994c5-136">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="994c5-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-137">Az.KeyVault</span></span>
* <span data-ttu-id="994c5-138">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-139">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="994c5-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="994c5-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="994c5-140">Az.MachineLearning</span></span>
* <span data-ttu-id="994c5-141">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="994c5-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="994c5-142">Az.Media</span></span>
* <span data-ttu-id="994c5-143">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="994c5-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="994c5-144">Az.Monitor</span></span>
  * <span data-ttu-id="994c5-145">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="994c5-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="994c5-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="994c5-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="994c5-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="994c5-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="994c5-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="994c5-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="994c5-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="994c5-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="994c5-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="994c5-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="994c5-151">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="994c5-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-152">Az.Network</span></span>
* <span data-ttu-id="994c5-153">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-154">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="994c5-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="994c5-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="994c5-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="994c5-156">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="994c5-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="994c5-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="994c5-158">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="994c5-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="994c5-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="994c5-160">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="994c5-162">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-163">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="994c5-164">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="994c5-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="994c5-165">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="994c5-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="994c5-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="994c5-166">Az.RedisCache</span></span>
* <span data-ttu-id="994c5-167">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-168">Az.Resources</span></span>
* <span data-ttu-id="994c5-169">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="994c5-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-170">Az.Sql</span></span>
* <span data-ttu-id="994c5-171">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="994c5-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="994c5-172">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-173">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="994c5-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="994c5-174">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="994c5-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="994c5-175">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="994c5-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="994c5-176">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="994c5-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="994c5-177">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="994c5-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-178">Az.Websites</span></span>
* <span data-ttu-id="994c5-179">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="994c5-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="994c5-180">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="994c5-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="994c5-181">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="994c5-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="994c5-182">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="994c5-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="994c5-183">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="994c5-184">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="994c5-184">Highlights since the last major release</span></span>
* <span data-ttu-id="994c5-185">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="994c5-185">General availability of `Az` module</span></span>
* <span data-ttu-id="994c5-186">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="994c5-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="994c5-187">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="994c5-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="994c5-188">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="994c5-189">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="994c5-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="994c5-190">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="994c5-191">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="994c5-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="994c5-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-192">Az.Accounts</span></span>
* <span data-ttu-id="994c5-193">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="994c5-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="994c5-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="994c5-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="994c5-195">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="994c5-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="994c5-196">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="994c5-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="994c5-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-197">Az.Automation</span></span>
* <span data-ttu-id="994c5-198">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="994c5-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="994c5-199">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="994c5-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="994c5-200">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-201">Az.Compute</span></span>
* <span data-ttu-id="994c5-202">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="994c5-203">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="994c5-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="994c5-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="994c5-205">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="994c5-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="994c5-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="994c5-206">Az.DataFactory</span></span>
* <span data-ttu-id="994c5-207">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="994c5-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="994c5-208">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="994c5-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-209">Az.Resources</span></span>
* <span data-ttu-id="994c5-210">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="994c5-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="994c5-211">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="994c5-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="994c5-212">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="994c5-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="994c5-213">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="994c5-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="994c5-214">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="994c5-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="994c5-215">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="994c5-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-216">Az.Sql</span></span>
* <span data-ttu-id="994c5-217">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="994c5-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="994c5-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-218">Az.Storage</span></span>
* <span data-ttu-id="994c5-219">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="994c5-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="994c5-220">New-AzStorageContext</span></span>
* <span data-ttu-id="994c5-221">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="994c5-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="994c5-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="994c5-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="994c5-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="994c5-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="994c5-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="994c5-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="994c5-226">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="994c5-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="994c5-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="994c5-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="994c5-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="994c5-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="994c5-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="994c5-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="994c5-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="994c5-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="994c5-231">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="994c5-232">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="994c5-232">Highlights since the last major release</span></span>
* <span data-ttu-id="994c5-233">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="994c5-233">General availability of `Az` module</span></span>
* <span data-ttu-id="994c5-234">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="994c5-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="994c5-235">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="994c5-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="994c5-236">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="994c5-237">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="994c5-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="994c5-238">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="994c5-239">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="994c5-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="994c5-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-240">Az.Automation</span></span>
* <span data-ttu-id="994c5-241">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="994c5-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="994c5-242">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="994c5-242">Dynamic grouping</span></span>
    * <span data-ttu-id="994c5-243">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="994c5-243">Pre-Post script</span></span>
    * <span data-ttu-id="994c5-244">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="994c5-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-245">Az.Compute</span></span>
* <span data-ttu-id="994c5-246">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="994c5-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="994c5-247">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="994c5-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="994c5-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-248">Az.KeyVault</span></span>
* <span data-ttu-id="994c5-249">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-250">Az.Network</span></span>
* <span data-ttu-id="994c5-251">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="994c5-252">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="994c5-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="994c5-254">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="994c5-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="994c5-255">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="994c5-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-256">Az.Resources</span></span>
* <span data-ttu-id="994c5-257">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="994c5-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="994c5-258">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="994c5-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-259">Az.Sql</span></span>
* <span data-ttu-id="994c5-260">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="994c5-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="994c5-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-261">Az.Storage</span></span>
* <span data-ttu-id="994c5-262">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="994c5-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="994c5-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="994c5-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="994c5-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="994c5-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="994c5-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="994c5-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="994c5-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="994c5-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="994c5-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-269">Az.Websites</span></span>
* <span data-ttu-id="994c5-270">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="994c5-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="994c5-271">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="994c5-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-272">Az.Accounts</span></span>
* <span data-ttu-id="994c5-273">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="994c5-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="994c5-274">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="994c5-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-275">Az.Automation</span></span>
* <span data-ttu-id="994c5-276">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="994c5-277">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="994c5-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="994c5-278">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="994c5-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="994c5-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="994c5-279">Az.Cdn</span></span>
* <span data-ttu-id="994c5-280">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="994c5-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-281">Az.Compute</span></span>
* <span data-ttu-id="994c5-282">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="994c5-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="994c5-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="994c5-283">Az.DataFactory</span></span>
* <span data-ttu-id="994c5-284">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="994c5-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="994c5-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="994c5-285">Az.LogicApp</span></span>
* <span data-ttu-id="994c5-286">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="994c5-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-287">Az.Network</span></span>
* <span data-ttu-id="994c5-288">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="994c5-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="994c5-290">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="994c5-291">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="994c5-291">SDK Update</span></span>
* <span data-ttu-id="994c5-292">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="994c5-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="994c5-293">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="994c5-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-294">Az.Resources</span></span>
* <span data-ttu-id="994c5-295">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="994c5-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="994c5-296">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="994c5-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="994c5-297">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="994c5-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="994c5-298">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="994c5-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="994c5-299">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="994c5-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="994c5-300">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="994c5-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-301">Az.Sql</span></span>
* <span data-ttu-id="994c5-302">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="994c5-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="994c5-303">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="994c5-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="994c5-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-304">Az.Storage</span></span>
* <span data-ttu-id="994c5-305">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="994c5-306">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="994c5-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="994c5-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="994c5-308">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="994c5-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-309">Az.Automation</span></span>
* <span data-ttu-id="994c5-310">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="994c5-311">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="994c5-312">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="994c5-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="994c5-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="994c5-314">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="994c5-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-315">Az.Compute</span></span>
* <span data-ttu-id="994c5-316">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="994c5-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="994c5-317">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="994c5-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="994c5-318">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="994c5-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="994c5-319">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="994c5-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-321">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="994c5-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="994c5-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="994c5-322">Az.EventHub</span></span>
* <span data-ttu-id="994c5-323">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="994c5-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="994c5-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-324">Az.KeyVault</span></span>
* <span data-ttu-id="994c5-325">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="994c5-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="994c5-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="994c5-326">Az.LogicApp</span></span>
* <span data-ttu-id="994c5-327">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="994c5-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="994c5-328">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="994c5-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="994c5-329">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="994c5-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="994c5-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="994c5-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="994c5-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="994c5-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="994c5-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="994c5-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="994c5-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="994c5-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="994c5-334">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="994c5-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="994c5-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="994c5-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="994c5-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="994c5-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="994c5-339">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="994c5-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="994c5-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="994c5-340">Az.Monitor</span></span>
* <span data-ttu-id="994c5-341">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="994c5-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-342">Az.Network</span></span>
* <span data-ttu-id="994c5-343">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="994c5-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="994c5-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="994c5-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="994c5-345">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="994c5-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="994c5-346">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="994c5-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="994c5-347">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="994c5-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-348">Az.Resources</span></span>
* <span data-ttu-id="994c5-349">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="994c5-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="994c5-350">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="994c5-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="994c5-351">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="994c5-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="994c5-352">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="994c5-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-353">Az.Sql</span></span>
* <span data-ttu-id="994c5-354">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="994c5-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="994c5-355">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="994c5-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-356">Az.Websites</span></span>
* <span data-ttu-id="994c5-357">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="994c5-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="994c5-358">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="994c5-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-359">Az.Accounts</span></span>
* <span data-ttu-id="994c5-360">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="994c5-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="994c5-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="994c5-361">Az.AnalysisServices</span></span>
<span data-ttu-id="994c5-362">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="994c5-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-363">Az.Compute</span></span>
* <span data-ttu-id="994c5-364">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="994c5-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="994c5-365">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="994c5-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="994c5-366">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="994c5-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-367">Az.RecoveryServices</span></span>
<span data-ttu-id="994c5-368">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="994c5-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-369">Az.Resources</span></span>
* <span data-ttu-id="994c5-370">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="994c5-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="994c5-371">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="994c5-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="994c5-372">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="994c5-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="994c5-373">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="994c5-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-374">Az.Sql</span></span>
* <span data-ttu-id="994c5-375">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="994c5-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="994c5-376">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="994c5-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="994c5-377">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="994c5-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="994c5-378">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="994c5-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-379">Az.Accounts</span></span>
* <span data-ttu-id="994c5-380">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="994c5-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="994c5-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="994c5-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="994c5-382">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="994c5-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="994c5-384">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="994c5-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="994c5-385">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="994c5-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-386">Az.Accounts</span></span>
* <span data-ttu-id="994c5-387">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="994c5-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="994c5-388">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="994c5-389">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="994c5-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="994c5-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="994c5-390">Az.Aks</span></span>
* <span data-ttu-id="994c5-391">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="994c5-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-392">Az.Automation</span></span>
* <span data-ttu-id="994c5-393">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="994c5-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="994c5-394">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="994c5-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="994c5-395">Az.Cdn</span></span>
* <span data-ttu-id="994c5-396">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-397">Az.Compute</span></span>
* <span data-ttu-id="994c5-398">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="994c5-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="994c5-399">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="994c5-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="994c5-400">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="994c5-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="994c5-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="994c5-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="994c5-402">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="994c5-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="994c5-403">Az.DataFactory</span></span>
* <span data-ttu-id="994c5-404">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="994c5-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-406">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="994c5-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="994c5-407">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="994c5-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="994c5-408">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="994c5-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="994c5-409">Az.IotHub</span></span>
* <span data-ttu-id="994c5-410">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="994c5-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="994c5-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-411">Az.KeyVault</span></span>
* <span data-ttu-id="994c5-412">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-413">Az.Network</span></span>
* <span data-ttu-id="994c5-414">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-415">Az.Resources</span></span>
* <span data-ttu-id="994c5-416">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="994c5-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="994c5-417">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="994c5-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="994c5-418">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="994c5-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="994c5-419">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="994c5-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="994c5-420">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="994c5-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="994c5-421">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="994c5-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="994c5-422">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="994c5-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="994c5-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="994c5-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="994c5-424">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="994c5-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="994c5-425">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="994c5-425">Fix some error messages.</span></span>
* <span data-ttu-id="994c5-426">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="994c5-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="994c5-427">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="994c5-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="994c5-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="994c5-428">Az.SignalR</span></span>
* <span data-ttu-id="994c5-429">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-430">Az.Sql</span></span>
* <span data-ttu-id="994c5-431">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="994c5-432">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="994c5-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="994c5-433">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="994c5-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="994c5-434">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="994c5-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="994c5-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-435">Az.Storage</span></span>
* <span data-ttu-id="994c5-436">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="994c5-437">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="994c5-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="994c5-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="994c5-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="994c5-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="994c5-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="994c5-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="994c5-440">Az.TrafficManager</span></span>
* <span data-ttu-id="994c5-441">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-442">Az.Websites</span></span>
* <span data-ttu-id="994c5-443">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="994c5-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="994c5-444">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="994c5-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="994c5-445">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="994c5-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="994c5-446">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="994c5-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="994c5-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-447">Az.Accounts</span></span>
* <span data-ttu-id="994c5-448">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="994c5-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-449">Az.Compute</span></span>
* <span data-ttu-id="994c5-450">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="994c5-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="994c5-451">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="994c5-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="994c5-452">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-454">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="994c5-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="994c5-455">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="994c5-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="994c5-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="994c5-456">Az.EventGrid</span></span>
* <span data-ttu-id="994c5-457">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="994c5-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="994c5-458">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="994c5-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="994c5-459">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="994c5-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="994c5-460">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="994c5-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="994c5-461">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="994c5-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="994c5-462">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="994c5-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="994c5-463">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="994c5-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="994c5-464">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="994c5-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="994c5-465">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="994c5-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="994c5-466">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="994c5-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="994c5-467">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="994c5-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="994c5-468">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="994c5-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="994c5-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="994c5-469">Az.IotHub</span></span>
* <span data-ttu-id="994c5-470">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="994c5-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="994c5-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="994c5-471">Az.LogicApp</span></span>
* <span data-ttu-id="994c5-472">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="994c5-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-473">Az.Resources</span></span>
* <span data-ttu-id="994c5-474">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="994c5-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="994c5-475">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="994c5-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="994c5-476">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994c5-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="994c5-477">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="994c5-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="994c5-478">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="994c5-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="994c5-479">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="994c5-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="994c5-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="994c5-480">Az.SignalR</span></span>
* <span data-ttu-id="994c5-481">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-482">Az.Sql</span></span>
* <span data-ttu-id="994c5-483">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="994c5-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="994c5-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-484">Az.Storage</span></span>
* <span data-ttu-id="994c5-485">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="994c5-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="994c5-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="994c5-486">New-AzStorageContext</span></span>
* <span data-ttu-id="994c5-487">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="994c5-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="994c5-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="994c5-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-489">Az.Websites</span></span>
* <span data-ttu-id="994c5-490">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="994c5-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="994c5-491">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="994c5-492">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="994c5-493">Geral</span><span class="sxs-lookup"><span data-stu-id="994c5-493">General</span></span>

- <span data-ttu-id="994c5-494">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="994c5-494">General Availability of Az Module</span></span>
- <span data-ttu-id="994c5-495">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="994c5-495">Online help for each module</span></span>
- <span data-ttu-id="994c5-496">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="994c5-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="994c5-497">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="994c5-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="994c5-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-498">Az.Accounts</span></span>
- <span data-ttu-id="994c5-499">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="994c5-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="994c5-500">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="994c5-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="994c5-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="994c5-501">Az.ApiManagement</span></span>
- <span data-ttu-id="994c5-502">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="994c5-502">Fixes for #7002</span></span>
- <span data-ttu-id="994c5-503">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="994c5-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="994c5-504">Az.Batch</span></span>
- <span data-ttu-id="994c5-505">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="994c5-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="994c5-506">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="994c5-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="994c5-507">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="994c5-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="994c5-508">Az.Billing</span></span>
- <span data-ttu-id="994c5-509">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="994c5-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="994c5-510">Az.CognitivServices</span></span>
- <span data-ttu-id="994c5-511">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="994c5-512">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="994c5-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="994c5-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="994c5-514">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="994c5-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="994c5-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="994c5-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="994c5-516">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="994c5-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="994c5-518">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="994c5-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="994c5-519">Az.Monitor</span></span>
- <span data-ttu-id="994c5-520">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="994c5-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="994c5-521">Az.KeyVault</span></span>
- <span data-ttu-id="994c5-522">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="994c5-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="994c5-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="994c5-523">Az.MachineLearning</span></span>
- <span data-ttu-id="994c5-524">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="994c5-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="994c5-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="994c5-525">Az.Media</span></span>
- <span data-ttu-id="994c5-526">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="994c5-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="994c5-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-527">Az.Network</span></span>
<span data-ttu-id="994c5-528">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="994c5-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="994c5-529">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="994c5-529">New cmdlets added:</span></span>
        - <span data-ttu-id="994c5-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="994c5-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="994c5-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="994c5-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="994c5-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="994c5-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="994c5-538">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="994c5-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="994c5-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="994c5-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="994c5-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="994c5-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="994c5-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="994c5-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="994c5-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="994c5-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="994c5-544">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="994c5-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="994c5-545">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="994c5-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="994c5-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="994c5-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="994c5-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="994c5-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="994c5-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="994c5-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="994c5-549">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="994c5-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="994c5-550">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="994c5-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="994c5-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="994c5-552">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="994c5-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="994c5-553">Az.Profile</span></span>
- <span data-ttu-id="994c5-554">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="994c5-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="994c5-556">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="994c5-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-557">Az.Resources</span></span>
- <span data-ttu-id="994c5-558">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="994c5-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="994c5-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="994c5-560">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="994c5-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="994c5-561">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="994c5-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="994c5-562">Az.SIgnalR</span></span>
- <span data-ttu-id="994c5-563">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="994c5-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="994c5-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-564">Az.Sql</span></span>
- <span data-ttu-id="994c5-565">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="994c5-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="994c5-566">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="994c5-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="994c5-567">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="994c5-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-568">Az.Storage</span></span>
- <span data-ttu-id="994c5-569">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="994c5-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-570">Az.Websites</span></span>
- <span data-ttu-id="994c5-571">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="994c5-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="994c5-572">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="994c5-573">Geral</span><span class="sxs-lookup"><span data-stu-id="994c5-573">General</span></span>

* <span data-ttu-id="994c5-574">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="994c5-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="994c5-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-575">Az.Compute</span></span>

* <span data-ttu-id="994c5-576">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="994c5-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="994c5-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="994c5-578">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="994c5-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="994c5-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="994c5-579">Az.FrontDoor</span></span>

* <span data-ttu-id="994c5-580">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="994c5-580">Fixed some broken links</span></span>
    - <span data-ttu-id="994c5-581">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="994c5-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="994c5-582">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="994c5-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="994c5-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="994c5-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="994c5-584">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="994c5-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="994c5-585">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="994c5-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="994c5-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-586">Az.Resources</span></span>

* <span data-ttu-id="994c5-587">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="994c5-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="994c5-588">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="994c5-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="994c5-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-589">Az.Sql</span></span>

* <span data-ttu-id="994c5-590">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="994c5-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="994c5-591">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="994c5-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="994c5-592">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="994c5-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="994c5-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-593">Az.Storage</span></span>

* <span data-ttu-id="994c5-594">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="994c5-595">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="994c5-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="994c5-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="994c5-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="994c5-597">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="994c5-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="994c5-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="994c5-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="994c5-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="994c5-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="994c5-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-600">Az.Websites</span></span>

* <span data-ttu-id="994c5-601">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="994c5-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="994c5-602">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="994c5-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="994c5-603">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="994c5-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="994c5-604">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="994c5-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="994c5-605">Az.ApiManagement</span></span>
* <span data-ttu-id="994c5-606">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="994c5-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="994c5-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="994c5-607">Az.Automation</span></span>
* <span data-ttu-id="994c5-608">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="994c5-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="994c5-609">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="994c5-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="994c5-610">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="994c5-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="994c5-611">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="994c5-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="994c5-612">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="994c5-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="994c5-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-613">Az.Compute</span></span>
* <span data-ttu-id="994c5-614">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="994c5-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="994c5-615">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="994c5-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="994c5-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="994c5-617">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="994c5-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="994c5-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="994c5-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="994c5-619">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="994c5-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="994c5-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-620">Az.Network</span></span>
* <span data-ttu-id="994c5-621">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="994c5-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="994c5-622">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="994c5-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="994c5-623">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="994c5-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="994c5-624">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="994c5-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="994c5-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="994c5-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="994c5-626">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="994c5-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="994c5-627">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="994c5-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="994c5-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="994c5-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="994c5-629">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="994c5-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="994c5-630">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="994c5-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="994c5-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="994c5-631">Az.Relay</span></span>
* <span data-ttu-id="994c5-632">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="994c5-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="994c5-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-633">Az.Resources</span></span>
* <span data-ttu-id="994c5-634">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="994c5-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="994c5-635">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="994c5-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="994c5-636">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="994c5-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="994c5-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="994c5-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="994c5-638">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="994c5-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="994c5-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-639">Az.Sql</span></span>
* <span data-ttu-id="994c5-640">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="994c5-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="994c5-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="994c5-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="994c5-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="994c5-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="994c5-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="994c5-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="994c5-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="994c5-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="994c5-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="994c5-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="994c5-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="994c5-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="994c5-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="994c5-649">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="994c5-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="994c5-650">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="994c5-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="994c5-651">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="994c5-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="994c5-652">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="994c5-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="994c5-653">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="994c5-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="994c5-654">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="994c5-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="994c5-655">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="994c5-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="994c5-656">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="994c5-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="994c5-657">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="994c5-658">Geral</span><span class="sxs-lookup"><span data-stu-id="994c5-658">General</span></span>
* <span data-ttu-id="994c5-659">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="994c5-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="994c5-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="994c5-660">Az.Profile</span></span>
* <span data-ttu-id="994c5-661">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="994c5-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="994c5-662">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="994c5-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="994c5-663">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="994c5-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="994c5-664">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="994c5-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="994c5-665">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="994c5-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="994c5-666">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="994c5-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="994c5-667">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="994c5-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="994c5-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="994c5-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="994c5-669">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="994c5-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-670">Az.Compute</span></span>
* <span data-ttu-id="994c5-671">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="994c5-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="994c5-672">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="994c5-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="994c5-673">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="994c5-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-675">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="994c5-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="994c5-676">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="994c5-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="994c5-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="994c5-677">Az.Insights</span></span>
* <span data-ttu-id="994c5-678">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="994c5-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="994c5-679">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="994c5-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="994c5-680">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="994c5-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="994c5-681">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="994c5-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-682">Az.Network</span></span>
* <span data-ttu-id="994c5-683">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="994c5-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="994c5-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="994c5-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="994c5-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="994c5-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="994c5-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="994c5-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="994c5-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="994c5-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="994c5-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="994c5-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="994c5-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="994c5-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="994c5-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="994c5-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="994c5-691">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="994c5-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-692">Az.Resources</span></span>
* <span data-ttu-id="994c5-693">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="994c5-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="994c5-694">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="994c5-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="994c5-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="994c5-695">Az.ServiceBus</span></span>
* <span data-ttu-id="994c5-696">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="994c5-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="994c5-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="994c5-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="994c5-698">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="994c5-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="994c5-699">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="994c5-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="994c5-700">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="994c5-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="994c5-701">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="994c5-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="994c5-702">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="994c5-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="994c5-703">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="994c5-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="994c5-704">Az.Profile</span></span>
* <span data-ttu-id="994c5-705">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="994c5-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="994c5-706">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="994c5-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-707">Az.Compute</span></span>
* <span data-ttu-id="994c5-708">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="994c5-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="994c5-709">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="994c5-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="994c5-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="994c5-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="994c5-711">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="994c5-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="994c5-712">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="994c5-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="994c5-713">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="994c5-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="994c5-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="994c5-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="994c5-715">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="994c5-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-716">Az.Network</span></span>
* <span data-ttu-id="994c5-717">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="994c5-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="994c5-718">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="994c5-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-719">Az.Resources</span></span>
* <span data-ttu-id="994c5-720">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="994c5-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="994c5-721">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="994c5-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="994c5-722">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="994c5-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="994c5-723">Azure.Storage</span></span>
* <span data-ttu-id="994c5-724">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="994c5-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="994c5-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="994c5-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="994c5-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="994c5-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="994c5-727">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="994c5-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="994c5-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="994c5-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="994c5-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="994c5-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="994c5-730">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="994c5-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="994c5-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="994c5-731">Az.Compute</span></span>
* <span data-ttu-id="994c5-732">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="994c5-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="994c5-733">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="994c5-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="994c5-734">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="994c5-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="994c5-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="994c5-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="994c5-736">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="994c5-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="994c5-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="994c5-737">Az.Network</span></span>
* <span data-ttu-id="994c5-738">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="994c5-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="994c5-739">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="994c5-739">new cmdlets added</span></span>
    - <span data-ttu-id="994c5-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="994c5-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="994c5-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="994c5-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="994c5-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="994c5-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="994c5-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="994c5-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="994c5-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="994c5-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="994c5-746">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="994c5-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="994c5-747">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="994c5-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="994c5-748">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="994c5-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="994c5-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="994c5-749">Az.RedisCache</span></span>
* <span data-ttu-id="994c5-750">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="994c5-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="994c5-751">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="994c5-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="994c5-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="994c5-752">Az.Resources</span></span>
* <span data-ttu-id="994c5-753">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="994c5-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="994c5-754">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="994c5-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="994c5-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="994c5-755">Az.Sql</span></span>
* <span data-ttu-id="994c5-756">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="994c5-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="994c5-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="994c5-757">Az.Websites</span></span>
* <span data-ttu-id="994c5-758">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="994c5-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="994c5-759">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="994c5-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="994c5-760">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="994c5-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="994c5-761">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="994c5-761">Initial Release</span></span>
