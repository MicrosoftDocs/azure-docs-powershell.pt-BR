---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882123"
---
## <a name="150---march-2019"></a><span data-ttu-id="28e0f-101">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="28e0f-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-102">Az.Accounts</span></span>
* <span data-ttu-id="28e0f-103">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="28e0f-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="28e0f-104">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="28e0f-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="28e0f-105">Az.Automation</span></span>
* <span data-ttu-id="28e0f-106">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="28e0f-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="28e0f-107">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="28e0f-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="28e0f-108">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="28e0f-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="28e0f-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="28e0f-109">Az.Cdn</span></span>
* <span data-ttu-id="28e0f-110">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="28e0f-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-111">Az.Compute</span></span>
* <span data-ttu-id="28e0f-112">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="28e0f-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="28e0f-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="28e0f-113">Az.DataFactory</span></span>
* <span data-ttu-id="28e0f-114">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="28e0f-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="28e0f-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="28e0f-115">Az.LogicApp</span></span>
* <span data-ttu-id="28e0f-116">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="28e0f-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-117">Az.Network</span></span>
* <span data-ttu-id="28e0f-118">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="28e0f-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="28e0f-120">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="28e0f-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="28e0f-121">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="28e0f-121">SDK Update</span></span>
* <span data-ttu-id="28e0f-122">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="28e0f-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="28e0f-123">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="28e0f-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-124">Az.Resources</span></span>
* <span data-ttu-id="28e0f-125">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="28e0f-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="28e0f-126">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="28e0f-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="28e0f-127">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="28e0f-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="28e0f-128">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="28e0f-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="28e0f-129">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="28e0f-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="28e0f-130">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="28e0f-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-131">Az.Sql</span></span>
* <span data-ttu-id="28e0f-132">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="28e0f-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="28e0f-133">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="28e0f-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="28e0f-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-134">Az.Storage</span></span>
* <span data-ttu-id="28e0f-135">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="28e0f-136">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="28e0f-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="28e0f-138">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="28e0f-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="28e0f-139">Az.Automation</span></span>
* <span data-ttu-id="28e0f-140">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="28e0f-141">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="28e0f-142">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="28e0f-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="28e0f-144">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="28e0f-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-145">Az.Compute</span></span>
* <span data-ttu-id="28e0f-146">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="28e0f-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="28e0f-147">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="28e0f-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="28e0f-148">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="28e0f-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="28e0f-149">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="28e0f-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="28e0f-151">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="28e0f-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="28e0f-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="28e0f-152">Az.EventHub</span></span>
* <span data-ttu-id="28e0f-153">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="28e0f-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="28e0f-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="28e0f-154">Az.KeyVault</span></span>
* <span data-ttu-id="28e0f-155">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="28e0f-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="28e0f-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="28e0f-156">Az.LogicApp</span></span>
* <span data-ttu-id="28e0f-157">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="28e0f-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="28e0f-158">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="28e0f-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="28e0f-159">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="28e0f-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="28e0f-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="28e0f-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="28e0f-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="28e0f-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="28e0f-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="28e0f-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="28e0f-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="28e0f-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="28e0f-164">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="28e0f-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="28e0f-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="28e0f-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="28e0f-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="28e0f-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="28e0f-169">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="28e0f-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="28e0f-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="28e0f-170">Az.Monitor</span></span>
* <span data-ttu-id="28e0f-171">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="28e0f-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-172">Az.Network</span></span>
* <span data-ttu-id="28e0f-173">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="28e0f-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="28e0f-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="28e0f-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="28e0f-175">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="28e0f-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="28e0f-176">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="28e0f-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="28e0f-177">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="28e0f-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="28e0f-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-178">Az.Resources</span></span>
* <span data-ttu-id="28e0f-179">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="28e0f-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="28e0f-180">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="28e0f-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="28e0f-181">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="28e0f-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="28e0f-182">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="28e0f-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-183">Az.Sql</span></span>
* <span data-ttu-id="28e0f-184">Adição de suporte para a camada de hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="28e0f-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="28e0f-185">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="28e0f-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="28e0f-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-186">Az.Websites</span></span>
* <span data-ttu-id="28e0f-187">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="28e0f-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="28e0f-188">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="28e0f-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-189">Az.Accounts</span></span>
* <span data-ttu-id="28e0f-190">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="28e0f-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="28e0f-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-191">Az.AnalysisServices</span></span>
<span data-ttu-id="28e0f-192">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="28e0f-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-193">Az.Compute</span></span>
* <span data-ttu-id="28e0f-194">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="28e0f-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="28e0f-195">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="28e0f-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="28e0f-196">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="28e0f-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="28e0f-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-197">Az.RecoveryServices</span></span>
<span data-ttu-id="28e0f-198">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="28e0f-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-199">Az.Resources</span></span>
* <span data-ttu-id="28e0f-200">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="28e0f-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="28e0f-201">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="28e0f-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="28e0f-202">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="28e0f-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="28e0f-203">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="28e0f-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-204">Az.Sql</span></span>
* <span data-ttu-id="28e0f-205">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="28e0f-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="28e0f-206">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="28e0f-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="28e0f-207">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="28e0f-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="28e0f-208">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="28e0f-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-209">Az.Accounts</span></span>
* <span data-ttu-id="28e0f-210">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="28e0f-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="28e0f-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="28e0f-212">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="28e0f-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="28e0f-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="28e0f-214">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="28e0f-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="28e0f-215">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="28e0f-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-216">Az.Accounts</span></span>
* <span data-ttu-id="28e0f-217">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="28e0f-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="28e0f-218">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="28e0f-219">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="28e0f-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="28e0f-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="28e0f-220">Az.Aks</span></span>
* <span data-ttu-id="28e0f-221">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="28e0f-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="28e0f-222">Az.Automation</span></span>
* <span data-ttu-id="28e0f-223">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="28e0f-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="28e0f-224">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="28e0f-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="28e0f-225">Az.Cdn</span></span>
* <span data-ttu-id="28e0f-226">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-227">Az.Compute</span></span>
* <span data-ttu-id="28e0f-228">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="28e0f-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="28e0f-229">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="28e0f-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="28e0f-230">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="28e0f-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="28e0f-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="28e0f-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="28e0f-232">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="28e0f-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="28e0f-233">Az.DataFactory</span></span>
* <span data-ttu-id="28e0f-234">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="28e0f-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="28e0f-236">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="28e0f-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="28e0f-237">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="28e0f-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="28e0f-238">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="28e0f-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="28e0f-239">Az.IotHub</span></span>
* <span data-ttu-id="28e0f-240">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="28e0f-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="28e0f-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="28e0f-241">Az.KeyVault</span></span>
* <span data-ttu-id="28e0f-242">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-243">Az.Network</span></span>
* <span data-ttu-id="28e0f-244">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-245">Az.Resources</span></span>
* <span data-ttu-id="28e0f-246">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="28e0f-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="28e0f-247">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28e0f-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="28e0f-248">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="28e0f-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="28e0f-249">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="28e0f-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="28e0f-250">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="28e0f-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="28e0f-251">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="28e0f-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="28e0f-252">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="28e0f-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="28e0f-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="28e0f-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="28e0f-254">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="28e0f-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="28e0f-255">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="28e0f-255">Fix some error messages.</span></span>
* <span data-ttu-id="28e0f-256">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="28e0f-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="28e0f-257">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="28e0f-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="28e0f-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="28e0f-258">Az.SignalR</span></span>
* <span data-ttu-id="28e0f-259">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-260">Az.Sql</span></span>
* <span data-ttu-id="28e0f-261">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="28e0f-262">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="28e0f-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="28e0f-263">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="28e0f-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="28e0f-264">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="28e0f-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="28e0f-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-265">Az.Storage</span></span>
* <span data-ttu-id="28e0f-266">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="28e0f-267">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="28e0f-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="28e0f-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="28e0f-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="28e0f-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="28e0f-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="28e0f-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="28e0f-270">Az.TrafficManager</span></span>
* <span data-ttu-id="28e0f-271">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="28e0f-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-272">Az.Websites</span></span>
* <span data-ttu-id="28e0f-273">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="28e0f-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="28e0f-274">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="28e0f-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="28e0f-275">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="28e0f-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="28e0f-276">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="28e0f-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="28e0f-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-277">Az.Accounts</span></span>
* <span data-ttu-id="28e0f-278">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="28e0f-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-279">Az.Compute</span></span>
* <span data-ttu-id="28e0f-280">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="28e0f-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="28e0f-281">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="28e0f-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="28e0f-282">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="28e0f-284">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="28e0f-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="28e0f-285">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="28e0f-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="28e0f-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="28e0f-286">Az.EventGrid</span></span>
* <span data-ttu-id="28e0f-287">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="28e0f-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="28e0f-288">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="28e0f-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="28e0f-289">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="28e0f-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="28e0f-290">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="28e0f-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="28e0f-291">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="28e0f-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="28e0f-292">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="28e0f-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="28e0f-293">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="28e0f-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="28e0f-294">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="28e0f-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="28e0f-295">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="28e0f-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="28e0f-296">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="28e0f-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="28e0f-297">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="28e0f-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="28e0f-298">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="28e0f-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="28e0f-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="28e0f-299">Az.IotHub</span></span>
* <span data-ttu-id="28e0f-300">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="28e0f-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="28e0f-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="28e0f-301">Az.LogicApp</span></span>
* <span data-ttu-id="28e0f-302">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="28e0f-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-303">Az.Resources</span></span>
* <span data-ttu-id="28e0f-304">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="28e0f-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="28e0f-305">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="28e0f-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="28e0f-306">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="28e0f-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="28e0f-307">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="28e0f-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="28e0f-308">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="28e0f-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="28e0f-309">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="28e0f-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="28e0f-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="28e0f-310">Az.SignalR</span></span>
* <span data-ttu-id="28e0f-311">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-312">Az.Sql</span></span>
* <span data-ttu-id="28e0f-313">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="28e0f-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="28e0f-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-314">Az.Storage</span></span>
* <span data-ttu-id="28e0f-315">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="28e0f-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="28e0f-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="28e0f-316">New-AzStorageContext</span></span>
* <span data-ttu-id="28e0f-317">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="28e0f-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="28e0f-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="28e0f-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="28e0f-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-319">Az.Websites</span></span>
* <span data-ttu-id="28e0f-320">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="28e0f-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="28e0f-321">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="28e0f-322">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="28e0f-323">Geral</span><span class="sxs-lookup"><span data-stu-id="28e0f-323">General</span></span>

- <span data-ttu-id="28e0f-324">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="28e0f-324">General Availability of Az Module</span></span>
- <span data-ttu-id="28e0f-325">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="28e0f-325">Online help for each module</span></span>
- <span data-ttu-id="28e0f-326">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="28e0f-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="28e0f-327">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="28e0f-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="28e0f-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-328">Az.Accounts</span></span>
- <span data-ttu-id="28e0f-329">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="28e0f-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="28e0f-330">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="28e0f-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="28e0f-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="28e0f-331">Az.ApiManagement</span></span>
- <span data-ttu-id="28e0f-332">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="28e0f-332">Fixes for #7002</span></span>
- <span data-ttu-id="28e0f-333">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="28e0f-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="28e0f-334">Az.Batch</span></span>
- <span data-ttu-id="28e0f-335">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="28e0f-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="28e0f-336">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="28e0f-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="28e0f-337">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="28e0f-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="28e0f-338">Az.Billing</span></span>
- <span data-ttu-id="28e0f-339">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="28e0f-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-340">Az.CognitivServices</span></span>
- <span data-ttu-id="28e0f-341">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="28e0f-342">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="28e0f-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="28e0f-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="28e0f-344">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="28e0f-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="28e0f-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="28e0f-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="28e0f-346">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="28e0f-348">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="28e0f-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="28e0f-349">Az.Monitor</span></span>
- <span data-ttu-id="28e0f-350">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="28e0f-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="28e0f-351">Az.KeyVault</span></span>
- <span data-ttu-id="28e0f-352">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="28e0f-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="28e0f-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="28e0f-353">Az.MachineLearning</span></span>
- <span data-ttu-id="28e0f-354">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="28e0f-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="28e0f-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="28e0f-355">Az.Media</span></span>
- <span data-ttu-id="28e0f-356">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="28e0f-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="28e0f-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-357">Az.Network</span></span>
<span data-ttu-id="28e0f-358">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="28e0f-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="28e0f-359">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="28e0f-359">New cmdlets added:</span></span>
        - <span data-ttu-id="28e0f-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="28e0f-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="28e0f-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="28e0f-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e0f-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="28e0f-368">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="28e0f-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="28e0f-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28e0f-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="28e0f-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="28e0f-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="28e0f-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="28e0f-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="28e0f-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="28e0f-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="28e0f-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28e0f-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="28e0f-374">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="28e0f-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="28e0f-375">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="28e0f-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="28e0f-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="28e0f-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="28e0f-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="28e0f-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="28e0f-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="28e0f-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="28e0f-379">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="28e0f-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="28e0f-380">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="28e0f-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="28e0f-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="28e0f-382">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="28e0f-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="28e0f-383">Az.Profile</span></span>
- <span data-ttu-id="28e0f-384">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="28e0f-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="28e0f-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="28e0f-386">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="28e0f-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-387">Az.Resources</span></span>
- <span data-ttu-id="28e0f-388">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="28e0f-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="28e0f-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="28e0f-390">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="28e0f-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="28e0f-391">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="28e0f-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="28e0f-392">Az.SIgnalR</span></span>
- <span data-ttu-id="28e0f-393">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="28e0f-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="28e0f-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-394">Az.Sql</span></span>
- <span data-ttu-id="28e0f-395">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="28e0f-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="28e0f-396">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="28e0f-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="28e0f-397">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="28e0f-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-398">Az.Storage</span></span>
- <span data-ttu-id="28e0f-399">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="28e0f-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-400">Az.Websites</span></span>
- <span data-ttu-id="28e0f-401">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="28e0f-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="28e0f-402">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="28e0f-403">Geral</span><span class="sxs-lookup"><span data-stu-id="28e0f-403">General</span></span>

* <span data-ttu-id="28e0f-404">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="28e0f-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="28e0f-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-405">Az.Compute</span></span>

* <span data-ttu-id="28e0f-406">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="28e0f-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="28e0f-408">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="28e0f-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="28e0f-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="28e0f-409">Az.FrontDoor</span></span>

* <span data-ttu-id="28e0f-410">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="28e0f-410">Fixed some broken links</span></span>
    - <span data-ttu-id="28e0f-411">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="28e0f-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="28e0f-412">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="28e0f-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="28e0f-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="28e0f-414">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="28e0f-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="28e0f-415">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="28e0f-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="28e0f-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-416">Az.Resources</span></span>

* <span data-ttu-id="28e0f-417">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="28e0f-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="28e0f-418">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="28e0f-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="28e0f-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-419">Az.Sql</span></span>

* <span data-ttu-id="28e0f-420">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="28e0f-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="28e0f-421">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="28e0f-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="28e0f-422">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="28e0f-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="28e0f-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-423">Az.Storage</span></span>

* <span data-ttu-id="28e0f-424">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="28e0f-425">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="28e0f-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="28e0f-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="28e0f-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="28e0f-427">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="28e0f-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="28e0f-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="28e0f-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="28e0f-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="28e0f-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="28e0f-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-430">Az.Websites</span></span>

* <span data-ttu-id="28e0f-431">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="28e0f-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="28e0f-432">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="28e0f-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="28e0f-433">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="28e0f-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="28e0f-434">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="28e0f-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="28e0f-435">Az.ApiManagement</span></span>
* <span data-ttu-id="28e0f-436">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="28e0f-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="28e0f-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="28e0f-437">Az.Automation</span></span>
* <span data-ttu-id="28e0f-438">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="28e0f-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="28e0f-439">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="28e0f-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="28e0f-440">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="28e0f-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="28e0f-441">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="28e0f-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="28e0f-442">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="28e0f-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="28e0f-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-443">Az.Compute</span></span>
* <span data-ttu-id="28e0f-444">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="28e0f-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="28e0f-445">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="28e0f-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="28e0f-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="28e0f-447">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="28e0f-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="28e0f-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="28e0f-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="28e0f-449">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="28e0f-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="28e0f-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-450">Az.Network</span></span>
* <span data-ttu-id="28e0f-451">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="28e0f-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="28e0f-452">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="28e0f-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="28e0f-453">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="28e0f-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="28e0f-454">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="28e0f-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="28e0f-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="28e0f-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="28e0f-456">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="28e0f-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="28e0f-457">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="28e0f-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="28e0f-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="28e0f-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="28e0f-459">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="28e0f-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="28e0f-460">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="28e0f-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="28e0f-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="28e0f-461">Az.Relay</span></span>
* <span data-ttu-id="28e0f-462">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="28e0f-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="28e0f-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-463">Az.Resources</span></span>
* <span data-ttu-id="28e0f-464">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="28e0f-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="28e0f-465">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="28e0f-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="28e0f-466">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="28e0f-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="28e0f-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="28e0f-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="28e0f-468">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="28e0f-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="28e0f-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-469">Az.Sql</span></span>
* <span data-ttu-id="28e0f-470">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="28e0f-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="28e0f-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="28e0f-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="28e0f-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="28e0f-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="28e0f-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="28e0f-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="28e0f-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="28e0f-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="28e0f-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="28e0f-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="28e0f-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="28e0f-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="28e0f-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="28e0f-479">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="28e0f-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="28e0f-480">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="28e0f-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="28e0f-481">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="28e0f-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="28e0f-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="28e0f-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="28e0f-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="28e0f-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="28e0f-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="28e0f-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="28e0f-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="28e0f-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="28e0f-486">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="28e0f-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="28e0f-487">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="28e0f-488">Geral</span><span class="sxs-lookup"><span data-stu-id="28e0f-488">General</span></span>
* <span data-ttu-id="28e0f-489">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="28e0f-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="28e0f-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="28e0f-490">Az.Profile</span></span>
* <span data-ttu-id="28e0f-491">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="28e0f-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="28e0f-492">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="28e0f-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="28e0f-493">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="28e0f-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="28e0f-494">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="28e0f-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="28e0f-495">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="28e0f-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="28e0f-496">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="28e0f-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="28e0f-497">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="28e0f-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="28e0f-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="28e0f-499">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="28e0f-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-500">Az.Compute</span></span>
* <span data-ttu-id="28e0f-501">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="28e0f-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="28e0f-502">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="28e0f-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="28e0f-503">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="28e0f-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="28e0f-505">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="28e0f-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="28e0f-506">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="28e0f-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="28e0f-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="28e0f-507">Az.Insights</span></span>
* <span data-ttu-id="28e0f-508">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="28e0f-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="28e0f-509">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="28e0f-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="28e0f-510">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="28e0f-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="28e0f-511">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="28e0f-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-512">Az.Network</span></span>
* <span data-ttu-id="28e0f-513">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="28e0f-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="28e0f-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="28e0f-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="28e0f-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="28e0f-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="28e0f-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="28e0f-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="28e0f-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="28e0f-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="28e0f-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="28e0f-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="28e0f-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="28e0f-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="28e0f-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="28e0f-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="28e0f-521">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="28e0f-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-522">Az.Resources</span></span>
* <span data-ttu-id="28e0f-523">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="28e0f-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="28e0f-524">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="28e0f-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="28e0f-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="28e0f-525">Az.ServiceBus</span></span>
* <span data-ttu-id="28e0f-526">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="28e0f-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="28e0f-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="28e0f-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="28e0f-528">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="28e0f-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="28e0f-529">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="28e0f-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="28e0f-530">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="28e0f-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="28e0f-531">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="28e0f-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="28e0f-532">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="28e0f-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="28e0f-533">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="28e0f-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="28e0f-534">Az.Profile</span></span>
* <span data-ttu-id="28e0f-535">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="28e0f-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="28e0f-536">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="28e0f-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-537">Az.Compute</span></span>
* <span data-ttu-id="28e0f-538">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="28e0f-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="28e0f-539">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="28e0f-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="28e0f-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28e0f-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="28e0f-541">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="28e0f-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="28e0f-542">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="28e0f-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="28e0f-543">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="28e0f-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="28e0f-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="28e0f-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="28e0f-545">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="28e0f-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-546">Az.Network</span></span>
* <span data-ttu-id="28e0f-547">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="28e0f-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="28e0f-548">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="28e0f-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-549">Az.Resources</span></span>
* <span data-ttu-id="28e0f-550">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="28e0f-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="28e0f-551">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="28e0f-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="28e0f-552">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="28e0f-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="28e0f-553">Azure.Storage</span></span>
* <span data-ttu-id="28e0f-554">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="28e0f-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="28e0f-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="28e0f-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="28e0f-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="28e0f-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="28e0f-557">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="28e0f-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="28e0f-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="28e0f-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="28e0f-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="28e0f-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="28e0f-560">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="28e0f-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="28e0f-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="28e0f-561">Az.Compute</span></span>
* <span data-ttu-id="28e0f-562">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="28e0f-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="28e0f-563">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="28e0f-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="28e0f-564">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="28e0f-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="28e0f-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="28e0f-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="28e0f-566">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="28e0f-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="28e0f-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="28e0f-567">Az.Network</span></span>
* <span data-ttu-id="28e0f-568">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="28e0f-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="28e0f-569">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="28e0f-569">new cmdlets added</span></span>
    - <span data-ttu-id="28e0f-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="28e0f-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="28e0f-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="28e0f-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="28e0f-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="28e0f-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="28e0f-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="28e0f-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="28e0f-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="28e0f-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="28e0f-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="28e0f-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="28e0f-576">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="28e0f-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="28e0f-577">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="28e0f-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="28e0f-578">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="28e0f-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="28e0f-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="28e0f-579">Az.RedisCache</span></span>
* <span data-ttu-id="28e0f-580">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="28e0f-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="28e0f-581">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="28e0f-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="28e0f-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="28e0f-582">Az.Resources</span></span>
* <span data-ttu-id="28e0f-583">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="28e0f-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="28e0f-584">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="28e0f-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="28e0f-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="28e0f-585">Az.Sql</span></span>
* <span data-ttu-id="28e0f-586">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="28e0f-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="28e0f-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="28e0f-587">Az.Websites</span></span>
* <span data-ttu-id="28e0f-588">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="28e0f-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="28e0f-589">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="28e0f-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="28e0f-590">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="28e0f-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="28e0f-591">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="28e0f-591">Initial Release</span></span>