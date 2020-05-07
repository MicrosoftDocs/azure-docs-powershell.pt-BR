---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "71319303"
---
## <a name="180---april-2019"></a><span data-ttu-id="5c568-103">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c568-104">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c568-104">Highlights since the last major release</span></span>
* <span data-ttu-id="5c568-105">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c568-105">General availability of `Az` module</span></span>
* <span data-ttu-id="5c568-106">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c568-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c568-107">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c568-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c568-108">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c568-109">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c568-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c568-110">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c568-111">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c568-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c568-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-112">Az.Accounts</span></span>
* <span data-ttu-id="5c568-113">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="5c568-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c568-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c568-114">Az.Batch</span></span>
* <span data-ttu-id="5c568-115">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c568-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c568-116">Az.Cdn</span></span>
* <span data-ttu-id="5c568-117">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c568-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c568-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c568-119">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-120">Az.Compute</span></span>
* <span data-ttu-id="5c568-121">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c568-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5c568-122">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-123">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c568-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c568-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c568-124">Az.DataFactory</span></span>
* <span data-ttu-id="5c568-125">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c568-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-127">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c568-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c568-128">Az.EventGrid</span></span>
* <span data-ttu-id="5c568-129">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="5c568-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c568-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c568-130">Az.EventHub</span></span>
* <span data-ttu-id="5c568-131">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="5c568-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5c568-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c568-132">Az.HDInsight</span></span>
* <span data-ttu-id="5c568-133">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c568-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c568-134">Az.IotHub</span></span>
* <span data-ttu-id="5c568-135">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c568-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-136">Az.KeyVault</span></span>
* <span data-ttu-id="5c568-137">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-138">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c568-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5c568-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c568-139">Az.MachineLearning</span></span>
* <span data-ttu-id="5c568-140">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5c568-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c568-141">Az.Media</span></span>
* <span data-ttu-id="5c568-142">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c568-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c568-143">Az.Monitor</span></span>
  * <span data-ttu-id="5c568-144">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="5c568-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5c568-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5c568-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5c568-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5c568-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5c568-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c568-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c568-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c568-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c568-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c568-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5c568-150">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="5c568-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-151">Az.Network</span></span>
* <span data-ttu-id="5c568-152">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-153">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c568-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5c568-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5c568-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="5c568-155">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c568-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c568-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c568-157">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5c568-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5c568-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5c568-159">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c568-161">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-162">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5c568-163">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5c568-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5c568-164">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="5c568-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c568-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c568-165">Az.RedisCache</span></span>
* <span data-ttu-id="5c568-166">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-167">Az.Resources</span></span>
* <span data-ttu-id="5c568-168">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c568-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-169">Az.Sql</span></span>
* <span data-ttu-id="5c568-170">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="5c568-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5c568-171">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-172">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="5c568-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5c568-173">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="5c568-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5c568-174">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="5c568-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5c568-175">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c568-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5c568-176">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c568-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-177">Az.Websites</span></span>
* <span data-ttu-id="5c568-178">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="5c568-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5c568-179">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c568-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c568-180">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="5c568-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5c568-181">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="5c568-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5c568-182">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c568-183">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c568-183">Highlights since the last major release</span></span>
* <span data-ttu-id="5c568-184">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c568-184">General availability of `Az` module</span></span>
* <span data-ttu-id="5c568-185">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c568-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c568-186">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c568-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c568-187">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c568-188">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c568-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c568-189">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c568-190">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c568-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c568-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-191">Az.Accounts</span></span>
* <span data-ttu-id="5c568-192">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="5c568-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c568-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c568-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c568-194">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="5c568-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5c568-195">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="5c568-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c568-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-196">Az.Automation</span></span>
* <span data-ttu-id="5c568-197">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="5c568-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5c568-198">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="5c568-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5c568-199">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-200">Az.Compute</span></span>
* <span data-ttu-id="5c568-201">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c568-202">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="5c568-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="5c568-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c568-204">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="5c568-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c568-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c568-205">Az.DataFactory</span></span>
* <span data-ttu-id="5c568-206">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="5c568-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5c568-207">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c568-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-208">Az.Resources</span></span>
* <span data-ttu-id="5c568-209">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="5c568-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5c568-210">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c568-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5c568-211">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="5c568-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5c568-212">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c568-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5c568-213">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="5c568-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5c568-214">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c568-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-215">Az.Sql</span></span>
* <span data-ttu-id="5c568-216">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="5c568-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c568-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-217">Az.Storage</span></span>
* <span data-ttu-id="5c568-218">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5c568-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c568-219">New-AzStorageContext</span></span>
* <span data-ttu-id="5c568-220">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c568-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5c568-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c568-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c568-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c568-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c568-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5c568-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5c568-225">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="5c568-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5c568-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c568-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c568-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c568-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c568-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c568-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5c568-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c568-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5c568-230">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c568-231">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c568-231">Highlights since the last major release</span></span>
* <span data-ttu-id="5c568-232">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c568-232">General availability of `Az` module</span></span>
* <span data-ttu-id="5c568-233">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c568-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c568-234">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c568-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c568-235">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c568-236">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c568-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c568-237">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c568-238">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c568-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c568-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-239">Az.Automation</span></span>
* <span data-ttu-id="5c568-240">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="5c568-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5c568-241">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c568-241">Dynamic grouping</span></span>
    * <span data-ttu-id="5c568-242">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="5c568-242">Pre-Post script</span></span>
    * <span data-ttu-id="5c568-243">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="5c568-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-244">Az.Compute</span></span>
* <span data-ttu-id="5c568-245">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5c568-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5c568-246">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c568-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c568-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-247">Az.KeyVault</span></span>
* <span data-ttu-id="5c568-248">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-249">Az.Network</span></span>
* <span data-ttu-id="5c568-250">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5c568-251">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="5c568-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c568-253">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c568-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5c568-254">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="5c568-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-255">Az.Resources</span></span>
* <span data-ttu-id="5c568-256">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c568-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5c568-257">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="5c568-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-258">Az.Sql</span></span>
* <span data-ttu-id="5c568-259">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="5c568-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c568-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-260">Az.Storage</span></span>
* <span data-ttu-id="5c568-261">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c568-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5c568-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c568-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c568-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c568-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5c568-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5c568-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5c568-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5c568-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5c568-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-268">Az.Websites</span></span>
* <span data-ttu-id="5c568-269">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="5c568-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="5c568-270">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c568-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-271">Az.Accounts</span></span>
* <span data-ttu-id="5c568-272">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="5c568-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5c568-273">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c568-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-274">Az.Automation</span></span>
* <span data-ttu-id="5c568-275">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c568-276">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="5c568-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5c568-277">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="5c568-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c568-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c568-278">Az.Cdn</span></span>
* <span data-ttu-id="5c568-279">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="5c568-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-280">Az.Compute</span></span>
* <span data-ttu-id="5c568-281">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="5c568-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c568-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c568-282">Az.DataFactory</span></span>
* <span data-ttu-id="5c568-283">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="5c568-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c568-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c568-284">Az.LogicApp</span></span>
* <span data-ttu-id="5c568-285">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="5c568-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-286">Az.Network</span></span>
* <span data-ttu-id="5c568-287">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="5c568-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c568-289">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5c568-290">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="5c568-290">SDK Update</span></span>
* <span data-ttu-id="5c568-291">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c568-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5c568-292">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c568-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-293">Az.Resources</span></span>
* <span data-ttu-id="5c568-294">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="5c568-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5c568-295">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="5c568-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5c568-296">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c568-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5c568-297">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="5c568-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5c568-298">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c568-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5c568-299">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="5c568-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-300">Az.Sql</span></span>
* <span data-ttu-id="5c568-301">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="5c568-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5c568-302">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c568-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c568-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-303">Az.Storage</span></span>
* <span data-ttu-id="5c568-304">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5c568-305">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5c568-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c568-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c568-307">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c568-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-308">Az.Automation</span></span>
* <span data-ttu-id="5c568-309">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5c568-310">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5c568-311">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c568-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c568-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c568-313">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="5c568-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-314">Az.Compute</span></span>
* <span data-ttu-id="5c568-315">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="5c568-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5c568-316">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="5c568-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5c568-317">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c568-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5c568-318">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="5c568-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-320">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="5c568-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c568-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c568-321">Az.EventHub</span></span>
* <span data-ttu-id="5c568-322">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="5c568-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5c568-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-323">Az.KeyVault</span></span>
* <span data-ttu-id="5c568-324">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c568-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c568-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c568-325">Az.LogicApp</span></span>
* <span data-ttu-id="5c568-326">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="5c568-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5c568-327">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="5c568-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5c568-328">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c568-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5c568-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c568-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c568-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c568-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c568-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c568-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c568-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c568-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5c568-333">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c568-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5c568-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c568-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c568-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c568-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5c568-338">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5c568-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c568-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c568-339">Az.Monitor</span></span>
* <span data-ttu-id="5c568-340">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5c568-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-341">Az.Network</span></span>
* <span data-ttu-id="5c568-342">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5c568-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c568-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c568-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c568-344">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="5c568-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5c568-345">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="5c568-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5c568-346">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="5c568-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5c568-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-347">Az.Resources</span></span>
* <span data-ttu-id="5c568-348">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c568-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c568-349">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c568-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5c568-350">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="5c568-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5c568-351">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5c568-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-352">Az.Sql</span></span>
* <span data-ttu-id="5c568-353">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5c568-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5c568-354">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="5c568-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-355">Az.Websites</span></span>
* <span data-ttu-id="5c568-356">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="5c568-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5c568-357">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c568-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-358">Az.Accounts</span></span>
* <span data-ttu-id="5c568-359">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c568-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c568-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c568-360">Az.AnalysisServices</span></span>
<span data-ttu-id="5c568-361">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="5c568-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-362">Az.Compute</span></span>
* <span data-ttu-id="5c568-363">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="5c568-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5c568-364">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5c568-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5c568-365">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c568-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-366">Az.RecoveryServices</span></span>
<span data-ttu-id="5c568-367">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="5c568-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-368">Az.Resources</span></span>
* <span data-ttu-id="5c568-369">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="5c568-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5c568-370">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c568-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c568-371">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="5c568-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5c568-372">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c568-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-373">Az.Sql</span></span>
* <span data-ttu-id="5c568-374">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c568-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5c568-375">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="5c568-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5c568-376">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5c568-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5c568-377">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c568-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-378">Az.Accounts</span></span>
* <span data-ttu-id="5c568-379">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="5c568-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c568-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c568-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c568-381">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c568-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c568-383">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c568-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5c568-384">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c568-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-385">Az.Accounts</span></span>
* <span data-ttu-id="5c568-386">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c568-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c568-387">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c568-388">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5c568-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c568-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c568-389">Az.Aks</span></span>
* <span data-ttu-id="5c568-390">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c568-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-391">Az.Automation</span></span>
* <span data-ttu-id="5c568-392">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="5c568-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5c568-393">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c568-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c568-394">Az.Cdn</span></span>
* <span data-ttu-id="5c568-395">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-396">Az.Compute</span></span>
* <span data-ttu-id="5c568-397">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="5c568-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5c568-398">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c568-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5c568-399">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c568-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c568-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c568-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c568-401">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c568-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c568-402">Az.DataFactory</span></span>
* <span data-ttu-id="5c568-403">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5c568-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-405">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c568-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5c568-406">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5c568-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5c568-407">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c568-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c568-408">Az.IotHub</span></span>
* <span data-ttu-id="5c568-409">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5c568-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c568-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-410">Az.KeyVault</span></span>
* <span data-ttu-id="5c568-411">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-412">Az.Network</span></span>
* <span data-ttu-id="5c568-413">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-414">Az.Resources</span></span>
* <span data-ttu-id="5c568-415">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="5c568-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5c568-416">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c568-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5c568-417">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="5c568-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5c568-418">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="5c568-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5c568-419">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="5c568-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5c568-420">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c568-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5c568-421">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5c568-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c568-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c568-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c568-423">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5c568-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5c568-424">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="5c568-424">Fix some error messages.</span></span>
* <span data-ttu-id="5c568-425">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="5c568-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5c568-426">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="5c568-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c568-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c568-427">Az.SignalR</span></span>
* <span data-ttu-id="5c568-428">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-429">Az.Sql</span></span>
* <span data-ttu-id="5c568-430">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c568-431">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5c568-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5c568-432">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="5c568-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5c568-433">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="5c568-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c568-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-434">Az.Storage</span></span>
* <span data-ttu-id="5c568-435">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c568-436">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c568-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5c568-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5c568-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5c568-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5c568-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5c568-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c568-439">Az.TrafficManager</span></span>
* <span data-ttu-id="5c568-440">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-441">Az.Websites</span></span>
* <span data-ttu-id="5c568-442">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c568-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c568-443">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="5c568-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5c568-444">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c568-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5c568-445">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c568-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c568-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-446">Az.Accounts</span></span>
* <span data-ttu-id="5c568-447">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5c568-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-448">Az.Compute</span></span>
* <span data-ttu-id="5c568-449">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5c568-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5c568-450">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c568-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5c568-451">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-453">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="5c568-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5c568-454">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="5c568-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c568-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c568-455">Az.EventGrid</span></span>
* <span data-ttu-id="5c568-456">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="5c568-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5c568-457">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5c568-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5c568-458">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c568-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c568-459">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c568-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c568-460">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c568-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c568-461">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c568-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5c568-462">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c568-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c568-463">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c568-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c568-464">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c568-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c568-465">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c568-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="5c568-466">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="5c568-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5c568-467">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c568-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c568-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c568-468">Az.IotHub</span></span>
* <span data-ttu-id="5c568-469">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="5c568-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c568-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c568-470">Az.LogicApp</span></span>
* <span data-ttu-id="5c568-471">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="5c568-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-472">Az.Resources</span></span>
* <span data-ttu-id="5c568-473">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="5c568-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5c568-474">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5c568-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5c568-475">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c568-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c568-476">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5c568-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5c568-477">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="5c568-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5c568-478">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5c568-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c568-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c568-479">Az.SignalR</span></span>
* <span data-ttu-id="5c568-480">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-481">Az.Sql</span></span>
* <span data-ttu-id="5c568-482">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="5c568-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c568-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-483">Az.Storage</span></span>
* <span data-ttu-id="5c568-484">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="5c568-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5c568-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c568-485">New-AzStorageContext</span></span>
* <span data-ttu-id="5c568-486">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c568-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5c568-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5c568-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-488">Az.Websites</span></span>
* <span data-ttu-id="5c568-489">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="5c568-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5c568-490">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5c568-491">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5c568-492">Geral</span><span class="sxs-lookup"><span data-stu-id="5c568-492">General</span></span>

- <span data-ttu-id="5c568-493">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="5c568-493">General Availability of Az Module</span></span>
- <span data-ttu-id="5c568-494">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="5c568-494">Online help for each module</span></span>
- <span data-ttu-id="5c568-495">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5c568-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5c568-496">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="5c568-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5c568-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-497">Az.Accounts</span></span>
- <span data-ttu-id="5c568-498">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c568-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="5c568-499">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="5c568-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c568-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c568-500">Az.ApiManagement</span></span>
- <span data-ttu-id="5c568-501">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="5c568-501">Fixes for #7002</span></span>
- <span data-ttu-id="5c568-502">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5c568-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c568-503">Az.Batch</span></span>
- <span data-ttu-id="5c568-504">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="5c568-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5c568-505">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="5c568-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5c568-506">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5c568-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c568-507">Az.Billing</span></span>
- <span data-ttu-id="5c568-508">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5c568-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5c568-509">Az.CognitivServices</span></span>
- <span data-ttu-id="5c568-510">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5c568-511">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="5c568-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c568-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="5c568-513">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c568-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5c568-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c568-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5c568-515">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c568-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="5c568-517">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5c568-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c568-518">Az.Monitor</span></span>
- <span data-ttu-id="5c568-519">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5c568-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c568-520">Az.KeyVault</span></span>
- <span data-ttu-id="5c568-521">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="5c568-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5c568-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c568-522">Az.MachineLearning</span></span>
- <span data-ttu-id="5c568-523">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="5c568-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5c568-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c568-524">Az.Media</span></span>
- <span data-ttu-id="5c568-525">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5c568-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c568-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-526">Az.Network</span></span>
<span data-ttu-id="5c568-527">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c568-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5c568-528">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c568-528">New cmdlets added:</span></span>
        - <span data-ttu-id="5c568-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5c568-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5c568-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5c568-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5c568-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c568-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5c568-537">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c568-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5c568-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c568-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5c568-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c568-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c568-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c568-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c568-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5c568-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5c568-543">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="5c568-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5c568-544">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c568-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5c568-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c568-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c568-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c568-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c568-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c568-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5c568-548">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c568-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5c568-549">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5c568-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c568-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="5c568-551">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5c568-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c568-552">Az.Profile</span></span>
- <span data-ttu-id="5c568-553">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c568-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="5c568-555">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5c568-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-556">Az.Resources</span></span>
- <span data-ttu-id="5c568-557">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c568-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c568-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="5c568-559">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="5c568-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5c568-560">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5c568-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c568-561">Az.SIgnalR</span></span>
- <span data-ttu-id="5c568-562">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c568-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5c568-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-563">Az.Sql</span></span>
- <span data-ttu-id="5c568-564">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="5c568-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5c568-565">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="5c568-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5c568-566">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c568-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-567">Az.Storage</span></span>
- <span data-ttu-id="5c568-568">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c568-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-569">Az.Websites</span></span>
- <span data-ttu-id="5c568-570">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c568-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5c568-571">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5c568-572">Geral</span><span class="sxs-lookup"><span data-stu-id="5c568-572">General</span></span>

* <span data-ttu-id="5c568-573">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c568-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c568-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-574">Az.Compute</span></span>

* <span data-ttu-id="5c568-575">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="5c568-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c568-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="5c568-577">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="5c568-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5c568-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c568-578">Az.FrontDoor</span></span>

* <span data-ttu-id="5c568-579">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="5c568-579">Fixed some broken links</span></span>
    - <span data-ttu-id="5c568-580">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="5c568-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5c568-581">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="5c568-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c568-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c568-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="5c568-583">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c568-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5c568-584">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="5c568-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c568-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-585">Az.Resources</span></span>

* <span data-ttu-id="5c568-586">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5c568-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5c568-587">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c568-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5c568-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-588">Az.Sql</span></span>

* <span data-ttu-id="5c568-589">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c568-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5c568-590">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="5c568-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5c568-591">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="5c568-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c568-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-592">Az.Storage</span></span>

* <span data-ttu-id="5c568-593">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5c568-594">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="5c568-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5c568-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c568-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c568-596">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="5c568-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="5c568-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c568-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5c568-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c568-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c568-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-599">Az.Websites</span></span>

* <span data-ttu-id="5c568-600">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c568-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5c568-601">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="5c568-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5c568-602">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c568-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5c568-603">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c568-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c568-604">Az.ApiManagement</span></span>
* <span data-ttu-id="5c568-605">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c568-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5c568-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c568-606">Az.Automation</span></span>
* <span data-ttu-id="5c568-607">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="5c568-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c568-608">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="5c568-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5c568-609">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="5c568-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5c568-610">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="5c568-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5c568-611">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="5c568-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c568-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-612">Az.Compute</span></span>
* <span data-ttu-id="5c568-613">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5c568-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5c568-614">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c568-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c568-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c568-616">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c568-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5c568-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5c568-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5c568-618">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="5c568-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c568-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-619">Az.Network</span></span>
* <span data-ttu-id="5c568-620">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="5c568-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5c568-621">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="5c568-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5c568-622">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="5c568-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5c568-623">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5c568-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5c568-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c568-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c568-625">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="5c568-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5c568-626">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c568-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5c568-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5c568-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5c568-628">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c568-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5c568-629">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c568-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5c568-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5c568-630">Az.Relay</span></span>
* <span data-ttu-id="5c568-631">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5c568-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c568-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-632">Az.Resources</span></span>
* <span data-ttu-id="5c568-633">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="5c568-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5c568-634">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="5c568-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5c568-635">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5c568-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c568-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c568-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c568-637">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="5c568-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5c568-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-638">Az.Sql</span></span>
* <span data-ttu-id="5c568-639">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="5c568-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5c568-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c568-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c568-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c568-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c568-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c568-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c568-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c568-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c568-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c568-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c568-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c568-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c568-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5c568-648">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c568-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5c568-649">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="5c568-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5c568-650">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="5c568-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5c568-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c568-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c568-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c568-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c568-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c568-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5c568-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c568-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5c568-655">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c568-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5c568-656">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5c568-657">Geral</span><span class="sxs-lookup"><span data-stu-id="5c568-657">General</span></span>
* <span data-ttu-id="5c568-658">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="5c568-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5c568-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c568-659">Az.Profile</span></span>
* <span data-ttu-id="5c568-660">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c568-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5c568-661">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="5c568-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5c568-662">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c568-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5c568-663">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="5c568-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5c568-664">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="5c568-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5c568-665">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c568-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5c568-666">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="5c568-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c568-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c568-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c568-668">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="5c568-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-669">Az.Compute</span></span>
* <span data-ttu-id="5c568-670">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c568-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5c568-671">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5c568-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5c568-672">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="5c568-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-674">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="5c568-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5c568-675">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="5c568-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5c568-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5c568-676">Az.Insights</span></span>
* <span data-ttu-id="5c568-677">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="5c568-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5c568-678">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="5c568-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5c568-679">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="5c568-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5c568-680">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="5c568-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-681">Az.Network</span></span>
* <span data-ttu-id="5c568-682">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="5c568-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5c568-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c568-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5c568-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5c568-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5c568-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c568-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5c568-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5c568-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5c568-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c568-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5c568-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c568-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c568-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c568-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c568-690">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="5c568-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-691">Az.Resources</span></span>
* <span data-ttu-id="5c568-692">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5c568-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5c568-693">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="5c568-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c568-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c568-694">Az.ServiceBus</span></span>
* <span data-ttu-id="5c568-695">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="5c568-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c568-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c568-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c568-697">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="5c568-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5c568-698">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="5c568-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5c568-699">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="5c568-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5c568-700">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5c568-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5c568-701">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="5c568-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5c568-702">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5c568-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c568-703">Az.Profile</span></span>
* <span data-ttu-id="5c568-704">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="5c568-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5c568-705">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c568-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-706">Az.Compute</span></span>
* <span data-ttu-id="5c568-707">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="5c568-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5c568-708">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c568-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c568-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c568-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c568-710">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c568-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5c568-711">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c568-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5c568-712">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c568-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c568-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c568-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c568-714">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c568-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-715">Az.Network</span></span>
* <span data-ttu-id="5c568-716">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="5c568-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5c568-717">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c568-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-718">Az.Resources</span></span>
* <span data-ttu-id="5c568-719">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="5c568-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5c568-720">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="5c568-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5c568-721">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5c568-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5c568-722">Azure.Storage</span></span>
* <span data-ttu-id="5c568-723">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="5c568-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5c568-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c568-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5c568-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c568-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c568-726">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5c568-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5c568-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5c568-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5c568-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c568-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c568-729">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="5c568-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c568-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c568-730">Az.Compute</span></span>
* <span data-ttu-id="5c568-731">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="5c568-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5c568-732">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5c568-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5c568-733">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="5c568-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5c568-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5c568-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5c568-735">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="5c568-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c568-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c568-736">Az.Network</span></span>
* <span data-ttu-id="5c568-737">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="5c568-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5c568-738">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="5c568-738">new cmdlets added</span></span>
    - <span data-ttu-id="5c568-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c568-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c568-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c568-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c568-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c568-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c568-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c568-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c568-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5c568-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5c568-745">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="5c568-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5c568-746">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c568-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5c568-747">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c568-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c568-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c568-748">Az.RedisCache</span></span>
* <span data-ttu-id="5c568-749">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="5c568-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5c568-750">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="5c568-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c568-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c568-751">Az.Resources</span></span>
* <span data-ttu-id="5c568-752">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c568-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c568-753">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="5c568-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c568-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c568-754">Az.Sql</span></span>
* <span data-ttu-id="5c568-755">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="5c568-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c568-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c568-756">Az.Websites</span></span>
* <span data-ttu-id="5c568-757">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="5c568-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5c568-758">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="5c568-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5c568-759">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c568-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5c568-760">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="5c568-760">Initial Release</span></span>