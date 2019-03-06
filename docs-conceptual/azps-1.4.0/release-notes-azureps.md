## <a name="140---february-2019"></a><span data-ttu-id="9fe2f-101">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="9fe2f-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="9fe2f-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="9fe2f-103">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="9fe2f-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9fe2f-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9fe2f-104">Az.Automation</span></span>
* <span data-ttu-id="9fe2f-105">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="9fe2f-106">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="9fe2f-107">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9fe2f-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="9fe2f-109">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-110">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-111">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="9fe2f-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="9fe2f-112">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="9fe2f-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="9fe2f-113">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="9fe2f-114">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="9fe2f-116">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9fe2f-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9fe2f-117">Az.EventHub</span></span>
* <span data-ttu-id="9fe2f-118">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="9fe2f-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="9fe2f-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fe2f-119">Az.KeyVault</span></span>
* <span data-ttu-id="9fe2f-120">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9fe2f-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9fe2f-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9fe2f-121">Az.LogicApp</span></span>
* <span data-ttu-id="9fe2f-122">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="9fe2f-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="9fe2f-123">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="9fe2f-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="9fe2f-124">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="9fe2f-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="9fe2f-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9fe2f-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9fe2f-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9fe2f-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9fe2f-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9fe2f-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9fe2f-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9fe2f-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="9fe2f-129">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="9fe2f-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="9fe2f-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9fe2f-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9fe2f-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9fe2f-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="9fe2f-134">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="9fe2f-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9fe2f-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9fe2f-135">Az.Monitor</span></span>
* <span data-ttu-id="9fe2f-136">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="9fe2f-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9fe2f-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-137">Az.Network</span></span>
* <span data-ttu-id="9fe2f-138">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9fe2f-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9fe2f-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9fe2f-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="9fe2f-140">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="9fe2f-141">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="9fe2f-142">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="9fe2f-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-143">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-144">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9fe2f-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9fe2f-145">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9fe2f-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="9fe2f-146">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="9fe2f-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="9fe2f-147">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="9fe2f-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="9fe2f-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-148">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-149">Adição de suporte para a camada de hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="9fe2f-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="9fe2f-150">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="9fe2f-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9fe2f-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-151">Az.Websites</span></span>
* <span data-ttu-id="9fe2f-152">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="9fe2f-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="9fe2f-153">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="9fe2f-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9fe2f-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-154">Az.Accounts</span></span>
* <span data-ttu-id="9fe2f-155">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9fe2f-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9fe2f-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-156">Az.AnalysisServices</span></span>
<span data-ttu-id="9fe2f-157">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-158">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-159">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="9fe2f-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="9fe2f-160">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9fe2f-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="9fe2f-161">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9fe2f-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-162">Az.RecoveryServices</span></span>
<span data-ttu-id="9fe2f-163">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-164">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-165">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="9fe2f-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="9fe2f-166">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9fe2f-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9fe2f-167">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="9fe2f-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="9fe2f-168">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9fe2f-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="9fe2f-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-169">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-170">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9fe2f-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="9fe2f-171">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="9fe2f-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="9fe2f-172">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="9fe2f-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="9fe2f-173">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="9fe2f-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9fe2f-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-174">Az.Accounts</span></span>
* <span data-ttu-id="9fe2f-175">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="9fe2f-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9fe2f-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="9fe2f-177">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="9fe2f-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9fe2f-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="9fe2f-179">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="9fe2f-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="9fe2f-180">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="9fe2f-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9fe2f-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-181">Az.Accounts</span></span>
* <span data-ttu-id="9fe2f-182">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="9fe2f-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9fe2f-183">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9fe2f-184">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9fe2f-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="9fe2f-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="9fe2f-185">Az.Aks</span></span>
* <span data-ttu-id="9fe2f-186">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9fe2f-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9fe2f-187">Az.Automation</span></span>
* <span data-ttu-id="9fe2f-188">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="9fe2f-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="9fe2f-189">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9fe2f-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9fe2f-190">Az.Cdn</span></span>
* <span data-ttu-id="9fe2f-191">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-192">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-193">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="9fe2f-194">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9fe2f-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="9fe2f-195">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fe2f-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="9fe2f-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9fe2f-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="9fe2f-197">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9fe2f-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9fe2f-198">Az.DataFactory</span></span>
* <span data-ttu-id="9fe2f-199">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="9fe2f-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="9fe2f-201">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="9fe2f-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="9fe2f-202">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="9fe2f-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="9fe2f-203">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9fe2f-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9fe2f-204">Az.IotHub</span></span>
* <span data-ttu-id="9fe2f-205">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9fe2f-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fe2f-206">Az.KeyVault</span></span>
* <span data-ttu-id="9fe2f-207">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9fe2f-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-208">Az.Network</span></span>
* <span data-ttu-id="9fe2f-209">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-210">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-211">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="9fe2f-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="9fe2f-212">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9fe2f-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="9fe2f-213">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="9fe2f-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="9fe2f-214">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="9fe2f-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="9fe2f-215">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="9fe2f-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="9fe2f-216">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="9fe2f-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="9fe2f-217">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="9fe2f-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9fe2f-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fe2f-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="9fe2f-219">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="9fe2f-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="9fe2f-220">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-220">Fix some error messages.</span></span>
* <span data-ttu-id="9fe2f-221">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="9fe2f-222">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9fe2f-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9fe2f-223">Az.SignalR</span></span>
* <span data-ttu-id="9fe2f-224">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="9fe2f-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-225">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-226">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9fe2f-227">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="9fe2f-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="9fe2f-228">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="9fe2f-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="9fe2f-229">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="9fe2f-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9fe2f-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-230">Az.Storage</span></span>
* <span data-ttu-id="9fe2f-231">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9fe2f-232">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="9fe2f-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9fe2f-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="9fe2f-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9fe2f-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="9fe2f-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9fe2f-235">Az.TrafficManager</span></span>
* <span data-ttu-id="9fe2f-236">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9fe2f-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-237">Az.Websites</span></span>
* <span data-ttu-id="9fe2f-238">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="9fe2f-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9fe2f-239">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="9fe2f-240">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="9fe2f-241">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="9fe2f-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9fe2f-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-242">Az.Accounts</span></span>
* <span data-ttu-id="9fe2f-243">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9fe2f-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-244">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-245">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="9fe2f-246">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="9fe2f-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="9fe2f-247">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="9fe2f-249">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="9fe2f-250">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="9fe2f-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9fe2f-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9fe2f-251">Az.EventGrid</span></span>
* <span data-ttu-id="9fe2f-252">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="9fe2f-253">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="9fe2f-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="9fe2f-254">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="9fe2f-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9fe2f-255">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="9fe2f-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9fe2f-256">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="9fe2f-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9fe2f-257">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="9fe2f-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="9fe2f-258">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="9fe2f-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9fe2f-259">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="9fe2f-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9fe2f-260">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="9fe2f-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9fe2f-261">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="9fe2f-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="9fe2f-262">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="9fe2f-263">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9fe2f-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9fe2f-264">Az.IotHub</span></span>
* <span data-ttu-id="9fe2f-265">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="9fe2f-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9fe2f-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9fe2f-266">Az.LogicApp</span></span>
* <span data-ttu-id="9fe2f-267">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="9fe2f-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-268">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-269">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="9fe2f-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="9fe2f-270">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="9fe2f-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="9fe2f-271">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9fe2f-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9fe2f-272">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9fe2f-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="9fe2f-273">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="9fe2f-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="9fe2f-274">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="9fe2f-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9fe2f-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9fe2f-275">Az.SignalR</span></span>
* <span data-ttu-id="9fe2f-276">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="9fe2f-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-277">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-278">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9fe2f-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-279">Az.Storage</span></span>
* <span data-ttu-id="9fe2f-280">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="9fe2f-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="9fe2f-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9fe2f-281">New-AzStorageContext</span></span>
* <span data-ttu-id="9fe2f-282">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="9fe2f-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9fe2f-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9fe2f-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-284">Az.Websites</span></span>
* <span data-ttu-id="9fe2f-285">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="9fe2f-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="9fe2f-286">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="9fe2f-287">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="9fe2f-288">Geral</span><span class="sxs-lookup"><span data-stu-id="9fe2f-288">General</span></span>

- <span data-ttu-id="9fe2f-289">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="9fe2f-289">General Availability of Az Module</span></span>
- <span data-ttu-id="9fe2f-290">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-290">Online help for each module</span></span>
- <span data-ttu-id="9fe2f-291">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="9fe2f-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="9fe2f-292">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="9fe2f-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="9fe2f-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-293">Az.Accounts</span></span>
- <span data-ttu-id="9fe2f-294">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="9fe2f-295">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="9fe2f-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9fe2f-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe2f-296">Az.ApiManagement</span></span>
- <span data-ttu-id="9fe2f-297">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="9fe2f-297">Fixes for #7002</span></span>
- <span data-ttu-id="9fe2f-298">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="9fe2f-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9fe2f-299">Az.Batch</span></span>
- <span data-ttu-id="9fe2f-300">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="9fe2f-301">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="9fe2f-302">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="9fe2f-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9fe2f-303">Az.Billing</span></span>
- <span data-ttu-id="9fe2f-304">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="9fe2f-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-305">Az.CognitivServices</span></span>
- <span data-ttu-id="9fe2f-306">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9fe2f-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="9fe2f-307">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="9fe2f-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9fe2f-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="9fe2f-309">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="9fe2f-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="9fe2f-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9fe2f-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="9fe2f-311">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="9fe2f-313">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="9fe2f-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9fe2f-314">Az.Monitor</span></span>
- <span data-ttu-id="9fe2f-315">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="9fe2f-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9fe2f-316">Az.KeyVault</span></span>
- <span data-ttu-id="9fe2f-317">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="9fe2f-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="9fe2f-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9fe2f-318">Az.MachineLearning</span></span>
- <span data-ttu-id="9fe2f-319">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="9fe2f-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9fe2f-320">Az.Media</span></span>
- <span data-ttu-id="9fe2f-321">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9fe2f-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9fe2f-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-322">Az.Network</span></span>
<span data-ttu-id="9fe2f-323">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="9fe2f-324">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="9fe2f-324">New cmdlets added:</span></span>
        - <span data-ttu-id="9fe2f-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9fe2f-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="9fe2f-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="9fe2f-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fe2f-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="9fe2f-333">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="9fe2f-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fe2f-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="9fe2f-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9fe2f-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9fe2f-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9fe2f-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9fe2f-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9fe2f-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="9fe2f-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9fe2f-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="9fe2f-339">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="9fe2f-340">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9fe2f-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="9fe2f-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9fe2f-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9fe2f-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9fe2f-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9fe2f-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9fe2f-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="9fe2f-344">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9fe2f-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="9fe2f-345">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="9fe2f-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9fe2f-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="9fe2f-347">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="9fe2f-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-348">Az.Profile</span></span>
- <span data-ttu-id="9fe2f-349">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9fe2f-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9fe2f-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="9fe2f-351">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="9fe2f-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-352">Az.Resources</span></span>
- <span data-ttu-id="9fe2f-353">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9fe2f-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fe2f-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="9fe2f-355">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="9fe2f-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="9fe2f-356">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="9fe2f-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9fe2f-357">Az.SIgnalR</span></span>
- <span data-ttu-id="9fe2f-358">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9fe2f-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="9fe2f-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-359">Az.Sql</span></span>
- <span data-ttu-id="9fe2f-360">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="9fe2f-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="9fe2f-361">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="9fe2f-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="9fe2f-362">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="9fe2f-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-363">Az.Storage</span></span>
- <span data-ttu-id="9fe2f-364">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9fe2f-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-365">Az.Websites</span></span>
- <span data-ttu-id="9fe2f-366">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="9fe2f-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="9fe2f-367">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="9fe2f-368">Geral</span><span class="sxs-lookup"><span data-stu-id="9fe2f-368">General</span></span>

* <span data-ttu-id="9fe2f-369">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="9fe2f-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="9fe2f-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-370">Az.Compute</span></span>

* <span data-ttu-id="9fe2f-371">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="9fe2f-373">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="9fe2f-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="9fe2f-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9fe2f-374">Az.FrontDoor</span></span>

* <span data-ttu-id="9fe2f-375">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="9fe2f-375">Fixed some broken links</span></span>
    - <span data-ttu-id="9fe2f-376">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="9fe2f-377">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9fe2f-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="9fe2f-379">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="9fe2f-380">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="9fe2f-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-381">Az.Resources</span></span>

* <span data-ttu-id="9fe2f-382">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="9fe2f-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="9fe2f-383">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="9fe2f-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-384">Az.Sql</span></span>

* <span data-ttu-id="9fe2f-385">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="9fe2f-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="9fe2f-386">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="9fe2f-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="9fe2f-387">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="9fe2f-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-388">Az.Storage</span></span>

* <span data-ttu-id="9fe2f-389">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9fe2f-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="9fe2f-390">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="9fe2f-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="9fe2f-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9fe2f-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9fe2f-392">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="9fe2f-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="9fe2f-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9fe2f-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="9fe2f-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9fe2f-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9fe2f-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-395">Az.Websites</span></span>

* <span data-ttu-id="9fe2f-396">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9fe2f-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="9fe2f-397">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="9fe2f-398">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="9fe2f-399">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9fe2f-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9fe2f-400">Az.ApiManagement</span></span>
* <span data-ttu-id="9fe2f-401">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="9fe2f-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9fe2f-402">Az.Automation</span></span>
* <span data-ttu-id="9fe2f-403">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="9fe2f-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="9fe2f-404">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="9fe2f-405">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="9fe2f-406">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="9fe2f-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="9fe2f-407">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="9fe2f-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="9fe2f-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-408">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-409">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="9fe2f-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="9fe2f-410">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9fe2f-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="9fe2f-412">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="9fe2f-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9fe2f-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9fe2f-414">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="9fe2f-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9fe2f-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-415">Az.Network</span></span>
* <span data-ttu-id="9fe2f-416">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="9fe2f-417">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe2f-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="9fe2f-418">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="9fe2f-419">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fe2f-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="9fe2f-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9fe2f-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9fe2f-421">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="9fe2f-422">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="9fe2f-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9fe2f-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9fe2f-424">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9fe2f-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="9fe2f-425">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="9fe2f-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="9fe2f-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9fe2f-426">Az.Relay</span></span>
* <span data-ttu-id="9fe2f-427">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="9fe2f-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-428">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-429">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="9fe2f-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="9fe2f-430">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="9fe2f-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="9fe2f-431">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="9fe2f-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9fe2f-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fe2f-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="9fe2f-433">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="9fe2f-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="9fe2f-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-434">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-435">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="9fe2f-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="9fe2f-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9fe2f-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9fe2f-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9fe2f-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9fe2f-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9fe2f-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe2f-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9fe2f-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe2f-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9fe2f-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe2f-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9fe2f-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9fe2f-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="9fe2f-444">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="9fe2f-445">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="9fe2f-446">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="9fe2f-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9fe2f-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9fe2f-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="9fe2f-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="9fe2f-451">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9fe2f-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="9fe2f-452">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9fe2f-453">Geral</span><span class="sxs-lookup"><span data-stu-id="9fe2f-453">General</span></span>
* <span data-ttu-id="9fe2f-454">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="9fe2f-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="9fe2f-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-455">Az.Profile</span></span>
* <span data-ttu-id="9fe2f-456">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9fe2f-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="9fe2f-457">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="9fe2f-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="9fe2f-458">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9fe2f-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="9fe2f-459">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="9fe2f-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="9fe2f-460">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="9fe2f-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="9fe2f-461">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="9fe2f-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="9fe2f-462">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="9fe2f-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="9fe2f-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="9fe2f-464">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-465">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-466">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9fe2f-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="9fe2f-467">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="9fe2f-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="9fe2f-468">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="9fe2f-470">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="9fe2f-471">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="9fe2f-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="9fe2f-472">Az.Insights</span></span>
* <span data-ttu-id="9fe2f-473">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="9fe2f-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="9fe2f-474">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="9fe2f-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="9fe2f-475">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="9fe2f-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="9fe2f-476">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="9fe2f-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9fe2f-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-477">Az.Network</span></span>
* <span data-ttu-id="9fe2f-478">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="9fe2f-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="9fe2f-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9fe2f-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="9fe2f-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9fe2f-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="9fe2f-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9fe2f-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="9fe2f-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9fe2f-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9fe2f-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9fe2f-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9fe2f-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9fe2f-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9fe2f-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9fe2f-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="9fe2f-486">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="9fe2f-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-487">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-488">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="9fe2f-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="9fe2f-489">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="9fe2f-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9fe2f-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9fe2f-490">Az.ServiceBus</span></span>
* <span data-ttu-id="9fe2f-491">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9fe2f-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9fe2f-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="9fe2f-493">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="9fe2f-494">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="9fe2f-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="9fe2f-495">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="9fe2f-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="9fe2f-496">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="9fe2f-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="9fe2f-497">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="9fe2f-498">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="9fe2f-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-499">Az.Profile</span></span>
* <span data-ttu-id="9fe2f-500">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="9fe2f-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="9fe2f-501">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9fe2f-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-502">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-503">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="9fe2f-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="9fe2f-504">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9fe2f-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9fe2f-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="9fe2f-506">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="9fe2f-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9fe2f-507">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9fe2f-508">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9fe2f-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9fe2f-510">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9fe2f-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-511">Az.Network</span></span>
* <span data-ttu-id="9fe2f-512">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9fe2f-513">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-514">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-515">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9fe2f-516">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="9fe2f-517">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9fe2f-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-518">Azure.Storage</span></span>
* <span data-ttu-id="9fe2f-519">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9fe2f-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9fe2f-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9fe2f-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9fe2f-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9fe2f-522">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9fe2f-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9fe2f-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="9fe2f-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9fe2f-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="9fe2f-525">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9fe2f-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9fe2f-526">Az.Compute</span></span>
* <span data-ttu-id="9fe2f-527">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="9fe2f-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9fe2f-528">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="9fe2f-529">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="9fe2f-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="9fe2f-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9fe2f-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="9fe2f-531">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9fe2f-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9fe2f-532">Az.Network</span></span>
* <span data-ttu-id="9fe2f-533">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9fe2f-534">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="9fe2f-534">new cmdlets added</span></span>
    - <span data-ttu-id="9fe2f-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="9fe2f-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="9fe2f-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="9fe2f-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9fe2f-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="9fe2f-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9fe2f-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="9fe2f-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fe2f-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9fe2f-541">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="9fe2f-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9fe2f-542">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fe2f-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="9fe2f-543">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9fe2f-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9fe2f-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9fe2f-544">Az.RedisCache</span></span>
* <span data-ttu-id="9fe2f-545">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="9fe2f-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9fe2f-546">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="9fe2f-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="9fe2f-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9fe2f-547">Az.Resources</span></span>
* <span data-ttu-id="9fe2f-548">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9fe2f-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9fe2f-549">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="9fe2f-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="9fe2f-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9fe2f-550">Az.Sql</span></span>
* <span data-ttu-id="9fe2f-551">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="9fe2f-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9fe2f-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9fe2f-552">Az.Websites</span></span>
* <span data-ttu-id="9fe2f-553">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="9fe2f-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9fe2f-554">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="9fe2f-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="9fe2f-555">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="9fe2f-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="9fe2f-556">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="9fe2f-556">Initial Release</span></span>