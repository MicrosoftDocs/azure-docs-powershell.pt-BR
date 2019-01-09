## <a name="100---december-2018"></a><span data-ttu-id="409d2-101">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="409d2-102">Geral</span><span class="sxs-lookup"><span data-stu-id="409d2-102">General</span></span>

- <span data-ttu-id="409d2-103">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="409d2-103">General Availability of Az Module</span></span>
- <span data-ttu-id="409d2-104">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="409d2-104">Online help for each module</span></span>
- <span data-ttu-id="409d2-105">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="409d2-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="409d2-106">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="409d2-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="409d2-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="409d2-107">Az.Accounts</span></span>
- <span data-ttu-id="409d2-108">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="409d2-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="409d2-109">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="409d2-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="409d2-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="409d2-110">Az.ApiManagement</span></span>
- <span data-ttu-id="409d2-111">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="409d2-111">Fixes for #7002</span></span>
- <span data-ttu-id="409d2-112">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="409d2-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="409d2-113">Az.Batch</span></span>
- <span data-ttu-id="409d2-114">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="409d2-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="409d2-115">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="409d2-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="409d2-116">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="409d2-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="409d2-117">Az.Billing</span></span>
- <span data-ttu-id="409d2-118">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="409d2-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="409d2-119">Az.CognitivServices</span></span>
- <span data-ttu-id="409d2-120">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="409d2-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="409d2-121">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="409d2-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="409d2-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="409d2-123">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="409d2-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="409d2-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="409d2-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="409d2-125">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="409d2-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="409d2-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="409d2-127">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="409d2-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="409d2-128">Az.Monitor</span></span>
- <span data-ttu-id="409d2-129">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="409d2-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="409d2-130">Az.KeyVault</span></span>
- <span data-ttu-id="409d2-131">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="409d2-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="409d2-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="409d2-132">Az.MachineLearning</span></span>
- <span data-ttu-id="409d2-133">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="409d2-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="409d2-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="409d2-134">Az.Media</span></span>
- <span data-ttu-id="409d2-135">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="409d2-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="409d2-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="409d2-136">Az.Network</span></span>
<span data-ttu-id="409d2-137">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="409d2-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="409d2-138">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="409d2-138">New cmdlets added:</span></span>
        - <span data-ttu-id="409d2-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="409d2-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="409d2-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="409d2-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="409d2-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="409d2-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="409d2-147">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="409d2-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="409d2-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="409d2-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="409d2-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="409d2-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="409d2-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="409d2-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="409d2-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="409d2-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="409d2-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="409d2-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="409d2-153">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="409d2-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="409d2-154">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="409d2-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="409d2-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="409d2-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="409d2-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="409d2-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="409d2-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="409d2-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="409d2-158">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="409d2-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="409d2-159">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="409d2-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="409d2-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="409d2-161">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="409d2-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="409d2-162">Az.Profile</span></span>
- <span data-ttu-id="409d2-163">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="409d2-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="409d2-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="409d2-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="409d2-165">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="409d2-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-166">Az.Resources</span></span>
- <span data-ttu-id="409d2-167">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="409d2-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="409d2-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="409d2-169">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="409d2-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="409d2-170">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="409d2-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="409d2-171">Az.SIgnalR</span></span>
- <span data-ttu-id="409d2-172">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="409d2-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="409d2-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="409d2-173">Az.Sql</span></span>
- <span data-ttu-id="409d2-174">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="409d2-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="409d2-175">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="409d2-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="409d2-176">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="409d2-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="409d2-177">Az.Storage</span></span>
- <span data-ttu-id="409d2-178">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="409d2-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="409d2-179">Az.Websites</span></span>
- <span data-ttu-id="409d2-180">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="409d2-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="409d2-181">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="409d2-182">Geral</span><span class="sxs-lookup"><span data-stu-id="409d2-182">General</span></span>

* <span data-ttu-id="409d2-183">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="409d2-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="409d2-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="409d2-184">Az.Compute</span></span>

* <span data-ttu-id="409d2-185">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="409d2-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="409d2-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="409d2-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="409d2-187">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="409d2-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="409d2-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="409d2-188">Az.FrontDoor</span></span>

* <span data-ttu-id="409d2-189">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="409d2-189">Fixed some broken links</span></span>
    - <span data-ttu-id="409d2-190">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="409d2-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="409d2-191">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="409d2-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="409d2-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="409d2-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="409d2-193">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="409d2-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="409d2-194">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="409d2-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="409d2-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-195">Az.Resources</span></span>

* <span data-ttu-id="409d2-196">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="409d2-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="409d2-197">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="409d2-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="409d2-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="409d2-198">Az.Sql</span></span>

* <span data-ttu-id="409d2-199">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="409d2-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="409d2-200">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="409d2-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="409d2-201">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="409d2-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="409d2-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="409d2-202">Az.Storage</span></span>

* <span data-ttu-id="409d2-203">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="409d2-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="409d2-204">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="409d2-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="409d2-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="409d2-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="409d2-206">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="409d2-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="409d2-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="409d2-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="409d2-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="409d2-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="409d2-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="409d2-209">Az.Websites</span></span>

* <span data-ttu-id="409d2-210">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="409d2-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="409d2-211">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="409d2-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="409d2-212">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="409d2-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="409d2-213">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="409d2-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="409d2-214">Az.ApiManagement</span></span>
* <span data-ttu-id="409d2-215">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="409d2-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="409d2-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="409d2-216">Az.Automation</span></span>
* <span data-ttu-id="409d2-217">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="409d2-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="409d2-218">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="409d2-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="409d2-219">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="409d2-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="409d2-220">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="409d2-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="409d2-221">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="409d2-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="409d2-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="409d2-222">Az.Compute</span></span>
* <span data-ttu-id="409d2-223">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="409d2-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="409d2-224">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="409d2-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="409d2-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="409d2-226">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="409d2-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="409d2-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="409d2-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="409d2-228">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="409d2-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="409d2-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="409d2-229">Az.Network</span></span>
* <span data-ttu-id="409d2-230">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="409d2-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="409d2-231">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="409d2-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="409d2-232">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="409d2-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="409d2-233">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="409d2-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="409d2-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="409d2-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="409d2-235">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="409d2-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="409d2-236">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="409d2-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="409d2-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="409d2-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="409d2-238">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="409d2-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="409d2-239">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="409d2-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="409d2-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="409d2-240">Az.Relay</span></span>
* <span data-ttu-id="409d2-241">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="409d2-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="409d2-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-242">Az.Resources</span></span>
* <span data-ttu-id="409d2-243">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="409d2-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="409d2-244">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="409d2-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="409d2-245">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="409d2-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="409d2-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="409d2-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="409d2-247">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="409d2-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="409d2-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="409d2-248">Az.Sql</span></span>
* <span data-ttu-id="409d2-249">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="409d2-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="409d2-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="409d2-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="409d2-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="409d2-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="409d2-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="409d2-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="409d2-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="409d2-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="409d2-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="409d2-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="409d2-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="409d2-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="409d2-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="409d2-258">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="409d2-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="409d2-259">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="409d2-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="409d2-260">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="409d2-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="409d2-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="409d2-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="409d2-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="409d2-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="409d2-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="409d2-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="409d2-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="409d2-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="409d2-265">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="409d2-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="409d2-266">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="409d2-267">Geral</span><span class="sxs-lookup"><span data-stu-id="409d2-267">General</span></span>
* <span data-ttu-id="409d2-268">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="409d2-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="409d2-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="409d2-269">Az.Profile</span></span>
* <span data-ttu-id="409d2-270">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="409d2-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="409d2-271">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="409d2-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="409d2-272">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="409d2-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="409d2-273">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="409d2-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="409d2-274">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="409d2-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="409d2-275">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="409d2-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="409d2-276">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="409d2-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="409d2-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="409d2-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="409d2-278">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="409d2-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="409d2-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="409d2-279">Az.Compute</span></span>
* <span data-ttu-id="409d2-280">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="409d2-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="409d2-281">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="409d2-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="409d2-282">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="409d2-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="409d2-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="409d2-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="409d2-284">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="409d2-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="409d2-285">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="409d2-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="409d2-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="409d2-286">Az.Insights</span></span>
* <span data-ttu-id="409d2-287">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="409d2-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="409d2-288">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="409d2-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="409d2-289">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="409d2-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="409d2-290">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="409d2-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="409d2-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="409d2-291">Az.Network</span></span>
* <span data-ttu-id="409d2-292">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="409d2-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="409d2-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="409d2-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="409d2-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="409d2-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="409d2-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="409d2-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="409d2-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="409d2-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="409d2-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="409d2-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="409d2-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="409d2-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="409d2-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="409d2-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="409d2-300">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="409d2-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="409d2-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-301">Az.Resources</span></span>
* <span data-ttu-id="409d2-302">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="409d2-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="409d2-303">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="409d2-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="409d2-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="409d2-304">Az.ServiceBus</span></span>
* <span data-ttu-id="409d2-305">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="409d2-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="409d2-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="409d2-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="409d2-307">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="409d2-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="409d2-308">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="409d2-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="409d2-309">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="409d2-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="409d2-310">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="409d2-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="409d2-311">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="409d2-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="409d2-312">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="409d2-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="409d2-313">Az.Profile</span></span>
* <span data-ttu-id="409d2-314">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="409d2-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="409d2-315">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="409d2-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="409d2-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="409d2-316">Az.Compute</span></span>
* <span data-ttu-id="409d2-317">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="409d2-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="409d2-318">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="409d2-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="409d2-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="409d2-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="409d2-320">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="409d2-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="409d2-321">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="409d2-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="409d2-322">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="409d2-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="409d2-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="409d2-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="409d2-324">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="409d2-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="409d2-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="409d2-325">Az.Network</span></span>
* <span data-ttu-id="409d2-326">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="409d2-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="409d2-327">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="409d2-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="409d2-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-328">Az.Resources</span></span>
* <span data-ttu-id="409d2-329">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="409d2-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="409d2-330">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="409d2-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="409d2-331">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="409d2-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="409d2-332">Azure.Storage</span></span>
* <span data-ttu-id="409d2-333">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="409d2-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="409d2-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="409d2-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="409d2-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="409d2-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="409d2-336">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="409d2-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="409d2-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="409d2-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="409d2-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="409d2-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="409d2-339">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="409d2-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="409d2-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="409d2-340">Az.Compute</span></span>
* <span data-ttu-id="409d2-341">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="409d2-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="409d2-342">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="409d2-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="409d2-343">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="409d2-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="409d2-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="409d2-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="409d2-345">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="409d2-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="409d2-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="409d2-346">Az.Network</span></span>
* <span data-ttu-id="409d2-347">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="409d2-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="409d2-348">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="409d2-348">new cmdlets added</span></span>
    - <span data-ttu-id="409d2-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="409d2-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="409d2-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="409d2-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="409d2-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="409d2-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="409d2-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="409d2-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="409d2-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="409d2-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="409d2-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="409d2-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="409d2-355">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="409d2-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="409d2-356">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="409d2-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="409d2-357">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="409d2-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="409d2-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="409d2-358">Az.RedisCache</span></span>
* <span data-ttu-id="409d2-359">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="409d2-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="409d2-360">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="409d2-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="409d2-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="409d2-361">Az.Resources</span></span>
* <span data-ttu-id="409d2-362">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="409d2-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="409d2-363">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="409d2-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="409d2-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="409d2-364">Az.Sql</span></span>
* <span data-ttu-id="409d2-365">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="409d2-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="409d2-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="409d2-366">Az.Websites</span></span>
* <span data-ttu-id="409d2-367">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="409d2-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="409d2-368">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="409d2-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="409d2-369">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="409d2-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="409d2-370">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="409d2-370">Initial Release</span></span>