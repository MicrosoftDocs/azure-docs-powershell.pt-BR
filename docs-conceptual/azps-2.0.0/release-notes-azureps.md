---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048624"
---
## <a name="200---may-2019"></a><span data-ttu-id="cb39f-101">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-102">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-103">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="cb39f-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb39f-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb39f-105">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="cb39f-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cb39f-106">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="cb39f-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-107">Az.Compute</span></span>
* <span data-ttu-id="cb39f-108">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="cb39f-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cb39f-109">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb39f-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cb39f-110">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cb39f-111">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cb39f-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cb39f-112">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cb39f-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cb39f-113">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb39f-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="cb39f-114">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="cb39f-114">Breaking changes</span></span>
    - <span data-ttu-id="cb39f-115">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cb39f-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cb39f-116">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="cb39f-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb39f-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb39f-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb39f-118">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb39f-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb39f-119">Az.Dns</span></span>
* <span data-ttu-id="cb39f-120">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="cb39f-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cb39f-121">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="cb39f-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cb39f-122">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="cb39f-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb39f-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb39f-123">Az.FrontDoor</span></span>
* <span data-ttu-id="cb39f-124">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cb39f-125">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="cb39f-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cb39f-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb39f-126">Az.HDInsight</span></span>
* <span data-ttu-id="cb39f-127">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cb39f-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cb39f-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb39f-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cb39f-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb39f-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb39f-130">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb39f-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb39f-131">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="cb39f-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cb39f-132">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="cb39f-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cb39f-133">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="cb39f-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb39f-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb39f-134">Az.Monitor</span></span>
* <span data-ttu-id="cb39f-135">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="cb39f-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="cb39f-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cb39f-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cb39f-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cb39f-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cb39f-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cb39f-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cb39f-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cb39f-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cb39f-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cb39f-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cb39f-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb39f-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cb39f-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb39f-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb39f-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb39f-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb39f-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb39f-147">[Mais](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="cb39f-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cb39f-148">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="cb39f-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-149">Az.Network</span></span>
* <span data-ttu-id="cb39f-150">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="cb39f-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cb39f-151">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="cb39f-151">New cmdlets</span></span>
        - <span data-ttu-id="cb39f-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb39f-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="cb39f-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb39f-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cb39f-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb39f-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cb39f-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb39f-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cb39f-156">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="cb39f-156">Updated cmdlets</span></span>
        - <span data-ttu-id="cb39f-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb39f-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cb39f-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb39f-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cb39f-159">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="cb39f-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cb39f-160">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="cb39f-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cb39f-161">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="cb39f-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb39f-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb39f-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb39f-163">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="cb39f-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cb39f-164">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cb39f-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cb39f-165">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="cb39f-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb39f-167">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb39f-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cb39f-168">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb39f-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cb39f-169">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cb39f-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cb39f-170">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb39f-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cb39f-171">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cb39f-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cb39f-172">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="cb39f-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cb39f-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb39f-173">Az.Relay</span></span>
* <span data-ttu-id="cb39f-174">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="cb39f-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb39f-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb39f-175">Az.ServiceBus</span></span>
* <span data-ttu-id="cb39f-176">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="cb39f-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-177">Az.Storage</span></span>
* <span data-ttu-id="cb39f-178">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage.*' para 'Microsoft.Azure.Storage.*')</span><span class="sxs-lookup"><span data-stu-id="cb39f-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cb39f-179">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="cb39f-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cb39f-180">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="cb39f-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cb39f-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb39f-182">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="cb39f-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cb39f-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cb39f-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cb39f-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-186">Az.Websites</span></span>
* <span data-ttu-id="cb39f-187">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cb39f-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cb39f-188">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="cb39f-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cb39f-189">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb39f-190">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="cb39f-190">Highlights since the last major release</span></span>
* <span data-ttu-id="cb39f-191">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="cb39f-191">General availability of `Az` module</span></span>
* <span data-ttu-id="cb39f-192">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb39f-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb39f-193">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb39f-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb39f-194">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb39f-195">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="cb39f-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb39f-196">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb39f-197">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="cb39f-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb39f-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-198">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-199">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="cb39f-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb39f-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb39f-200">Az.Batch</span></span>
* <span data-ttu-id="cb39f-201">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb39f-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb39f-202">Az.Cdn</span></span>
* <span data-ttu-id="cb39f-203">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb39f-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb39f-205">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-206">Az.Compute</span></span>
* <span data-ttu-id="cb39f-207">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="cb39f-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cb39f-208">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-209">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="cb39f-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb39f-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb39f-210">Az.DataFactory</span></span>
* <span data-ttu-id="cb39f-211">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cb39f-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-213">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb39f-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb39f-214">Az.EventGrid</span></span>
* <span data-ttu-id="cb39f-215">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="cb39f-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb39f-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-216">Az.EventHub</span></span>
* <span data-ttu-id="cb39f-217">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="cb39f-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cb39f-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb39f-218">Az.HDInsight</span></span>
* <span data-ttu-id="cb39f-219">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb39f-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-220">Az.IotHub</span></span>
* <span data-ttu-id="cb39f-221">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb39f-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-222">Az.KeyVault</span></span>
* <span data-ttu-id="cb39f-223">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-224">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="cb39f-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb39f-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb39f-225">Az.MachineLearning</span></span>
* <span data-ttu-id="cb39f-226">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cb39f-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb39f-227">Az.Media</span></span>
* <span data-ttu-id="cb39f-228">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb39f-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb39f-229">Az.Monitor</span></span>
  * <span data-ttu-id="cb39f-230">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="cb39f-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cb39f-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cb39f-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cb39f-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cb39f-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cb39f-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb39f-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb39f-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb39f-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb39f-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb39f-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cb39f-236">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="cb39f-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-237">Az.Network</span></span>
* <span data-ttu-id="cb39f-238">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-239">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="cb39f-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cb39f-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cb39f-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="cb39f-241">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb39f-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb39f-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb39f-243">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb39f-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb39f-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb39f-245">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb39f-247">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-248">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cb39f-249">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="cb39f-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cb39f-250">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="cb39f-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb39f-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb39f-251">Az.RedisCache</span></span>
* <span data-ttu-id="cb39f-252">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-253">Az.Resources</span></span>
* <span data-ttu-id="cb39f-254">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="cb39f-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-255">Az.Sql</span></span>
* <span data-ttu-id="cb39f-256">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="cb39f-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cb39f-257">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-258">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="cb39f-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cb39f-259">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="cb39f-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cb39f-260">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="cb39f-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cb39f-261">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="cb39f-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cb39f-262">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="cb39f-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-263">Az.Websites</span></span>
* <span data-ttu-id="cb39f-264">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="cb39f-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cb39f-265">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb39f-266">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="cb39f-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cb39f-267">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cb39f-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cb39f-268">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb39f-269">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="cb39f-269">Highlights since the last major release</span></span>
* <span data-ttu-id="cb39f-270">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="cb39f-270">General availability of `Az` module</span></span>
* <span data-ttu-id="cb39f-271">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb39f-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb39f-272">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb39f-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb39f-273">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb39f-274">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="cb39f-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb39f-275">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb39f-276">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="cb39f-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb39f-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-277">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-278">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="cb39f-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb39f-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb39f-280">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="cb39f-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cb39f-281">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="cb39f-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb39f-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-282">Az.Automation</span></span>
* <span data-ttu-id="cb39f-283">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="cb39f-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cb39f-284">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="cb39f-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cb39f-285">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-286">Az.Compute</span></span>
* <span data-ttu-id="cb39f-287">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb39f-288">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="cb39f-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb39f-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb39f-290">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="cb39f-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb39f-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb39f-291">Az.DataFactory</span></span>
* <span data-ttu-id="cb39f-292">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="cb39f-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cb39f-293">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cb39f-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-294">Az.Resources</span></span>
* <span data-ttu-id="cb39f-295">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="cb39f-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cb39f-296">Melhorar o tratamento de erros para “Test-AzDeployment” e “Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cb39f-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb39f-297">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="cb39f-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cb39f-298">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb39f-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cb39f-299">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="cb39f-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cb39f-300">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb39f-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-301">Az.Sql</span></span>
* <span data-ttu-id="cb39f-302">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="cb39f-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-303">Az.Storage</span></span>
* <span data-ttu-id="cb39f-304">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cb39f-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb39f-305">New-AzStorageContext</span></span>
* <span data-ttu-id="cb39f-306">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cb39f-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cb39f-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb39f-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb39f-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb39f-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb39f-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cb39f-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cb39f-311">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="cb39f-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cb39f-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb39f-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb39f-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb39f-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb39f-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb39f-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cb39f-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb39f-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cb39f-316">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb39f-317">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="cb39f-317">Highlights since the last major release</span></span>
* <span data-ttu-id="cb39f-318">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="cb39f-318">General availability of `Az` module</span></span>
* <span data-ttu-id="cb39f-319">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb39f-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb39f-320">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb39f-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb39f-321">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb39f-322">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="cb39f-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb39f-323">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb39f-324">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="cb39f-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb39f-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-325">Az.Automation</span></span>
* <span data-ttu-id="cb39f-326">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="cb39f-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cb39f-327">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="cb39f-327">Dynamic grouping</span></span>
    * <span data-ttu-id="cb39f-328">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="cb39f-328">Pre-Post script</span></span>
    * <span data-ttu-id="cb39f-329">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="cb39f-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-330">Az.Compute</span></span>
* <span data-ttu-id="cb39f-331">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cb39f-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cb39f-332">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="cb39f-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb39f-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-333">Az.KeyVault</span></span>
* <span data-ttu-id="cb39f-334">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-335">Az.Network</span></span>
* <span data-ttu-id="cb39f-336">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cb39f-337">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="cb39f-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb39f-339">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="cb39f-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cb39f-340">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="cb39f-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-341">Az.Resources</span></span>
* <span data-ttu-id="cb39f-342">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb39f-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cb39f-343">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="cb39f-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-344">Az.Sql</span></span>
* <span data-ttu-id="cb39f-345">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="cb39f-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-346">Az.Storage</span></span>
* <span data-ttu-id="cb39f-347">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="cb39f-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cb39f-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb39f-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb39f-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb39f-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cb39f-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cb39f-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cb39f-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cb39f-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-354">Az.Websites</span></span>
* <span data-ttu-id="cb39f-355">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="cb39f-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="cb39f-356">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-357">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-358">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="cb39f-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cb39f-359">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb39f-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-360">Az.Automation</span></span>
* <span data-ttu-id="cb39f-361">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb39f-362">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="cb39f-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cb39f-363">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="cb39f-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb39f-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb39f-364">Az.Cdn</span></span>
* <span data-ttu-id="cb39f-365">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="cb39f-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-366">Az.Compute</span></span>
* <span data-ttu-id="cb39f-367">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="cb39f-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb39f-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb39f-368">Az.DataFactory</span></span>
* <span data-ttu-id="cb39f-369">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="cb39f-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb39f-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb39f-370">Az.LogicApp</span></span>
* <span data-ttu-id="cb39f-371">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="cb39f-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-372">Az.Network</span></span>
* <span data-ttu-id="cb39f-373">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb39f-375">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cb39f-376">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="cb39f-376">SDK Update</span></span>
* <span data-ttu-id="cb39f-377">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb39f-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cb39f-378">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb39f-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-379">Az.Resources</span></span>
* <span data-ttu-id="cb39f-380">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="cb39f-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cb39f-381">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cb39f-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cb39f-382">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cb39f-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cb39f-383">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cb39f-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cb39f-384">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cb39f-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cb39f-385">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cb39f-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-386">Az.Sql</span></span>
* <span data-ttu-id="cb39f-387">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="cb39f-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cb39f-388">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="cb39f-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-389">Az.Storage</span></span>
* <span data-ttu-id="cb39f-390">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cb39f-391">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cb39f-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb39f-393">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb39f-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-394">Az.Automation</span></span>
* <span data-ttu-id="cb39f-395">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cb39f-396">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cb39f-397">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb39f-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb39f-399">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="cb39f-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-400">Az.Compute</span></span>
* <span data-ttu-id="cb39f-401">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="cb39f-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cb39f-402">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="cb39f-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cb39f-403">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cb39f-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cb39f-404">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="cb39f-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-406">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="cb39f-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb39f-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-407">Az.EventHub</span></span>
* <span data-ttu-id="cb39f-408">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="cb39f-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-409">Az.KeyVault</span></span>
* <span data-ttu-id="cb39f-410">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cb39f-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb39f-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb39f-411">Az.LogicApp</span></span>
* <span data-ttu-id="cb39f-412">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="cb39f-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cb39f-413">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="cb39f-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cb39f-414">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="cb39f-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cb39f-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb39f-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb39f-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb39f-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb39f-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb39f-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb39f-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb39f-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cb39f-419">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="cb39f-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cb39f-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb39f-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb39f-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb39f-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cb39f-424">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="cb39f-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb39f-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb39f-425">Az.Monitor</span></span>
* <span data-ttu-id="cb39f-426">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="cb39f-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-427">Az.Network</span></span>
* <span data-ttu-id="cb39f-428">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="cb39f-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb39f-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb39f-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb39f-430">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="cb39f-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cb39f-431">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="cb39f-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="cb39f-432">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="cb39f-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="cb39f-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-433">Az.Resources</span></span>
* <span data-ttu-id="cb39f-434">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cb39f-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb39f-435">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cb39f-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cb39f-436">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="cb39f-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cb39f-437">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="cb39f-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-438">Az.Sql</span></span>
* <span data-ttu-id="cb39f-439">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cb39f-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cb39f-440">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="cb39f-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-441">Az.Websites</span></span>
* <span data-ttu-id="cb39f-442">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="cb39f-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cb39f-443">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-444">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-445">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb39f-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb39f-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-446">Az.AnalysisServices</span></span>
<span data-ttu-id="cb39f-447">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="cb39f-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-448">Az.Compute</span></span>
* <span data-ttu-id="cb39f-449">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="cb39f-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cb39f-450">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cb39f-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cb39f-451">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cb39f-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-452">Az.RecoveryServices</span></span>
<span data-ttu-id="cb39f-453">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="cb39f-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-454">Az.Resources</span></span>
* <span data-ttu-id="cb39f-455">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="cb39f-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="cb39f-456">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cb39f-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb39f-457">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="cb39f-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="cb39f-458">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cb39f-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-459">Az.Sql</span></span>
* <span data-ttu-id="cb39f-460">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb39f-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cb39f-461">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="cb39f-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cb39f-462">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="cb39f-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cb39f-463">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-464">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-465">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="cb39f-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb39f-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb39f-467">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="cb39f-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb39f-469">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="cb39f-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cb39f-470">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-471">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-472">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="cb39f-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb39f-473">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb39f-474">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="cb39f-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb39f-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb39f-475">Az.Aks</span></span>
* <span data-ttu-id="cb39f-476">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb39f-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-477">Az.Automation</span></span>
* <span data-ttu-id="cb39f-478">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="cb39f-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cb39f-479">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb39f-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb39f-480">Az.Cdn</span></span>
* <span data-ttu-id="cb39f-481">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-482">Az.Compute</span></span>
* <span data-ttu-id="cb39f-483">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="cb39f-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cb39f-484">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb39f-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cb39f-485">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb39f-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb39f-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb39f-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb39f-487">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb39f-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb39f-488">Az.DataFactory</span></span>
* <span data-ttu-id="cb39f-489">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="cb39f-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-491">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="cb39f-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cb39f-492">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cb39f-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cb39f-493">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb39f-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-494">Az.IotHub</span></span>
* <span data-ttu-id="cb39f-495">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cb39f-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb39f-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-496">Az.KeyVault</span></span>
* <span data-ttu-id="cb39f-497">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-498">Az.Network</span></span>
* <span data-ttu-id="cb39f-499">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-500">Az.Resources</span></span>
* <span data-ttu-id="cb39f-501">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="cb39f-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cb39f-502">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cb39f-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cb39f-503">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="cb39f-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cb39f-504">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="cb39f-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cb39f-505">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="cb39f-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cb39f-506">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="cb39f-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cb39f-507">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cb39f-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb39f-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb39f-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb39f-509">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cb39f-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cb39f-510">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="cb39f-510">Fix some error messages.</span></span>
* <span data-ttu-id="cb39f-511">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="cb39f-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cb39f-512">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="cb39f-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb39f-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb39f-513">Az.SignalR</span></span>
* <span data-ttu-id="cb39f-514">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-515">Az.Sql</span></span>
* <span data-ttu-id="cb39f-516">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb39f-517">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="cb39f-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cb39f-518">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="cb39f-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cb39f-519">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="cb39f-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-520">Az.Storage</span></span>
* <span data-ttu-id="cb39f-521">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb39f-522">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cb39f-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cb39f-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cb39f-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cb39f-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb39f-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb39f-525">Az.TrafficManager</span></span>
* <span data-ttu-id="cb39f-526">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-527">Az.Websites</span></span>
* <span data-ttu-id="cb39f-528">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="cb39f-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb39f-529">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="cb39f-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cb39f-530">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb39f-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cb39f-531">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="cb39f-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb39f-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-532">Az.Accounts</span></span>
* <span data-ttu-id="cb39f-533">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="cb39f-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-534">Az.Compute</span></span>
* <span data-ttu-id="cb39f-535">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cb39f-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cb39f-536">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="cb39f-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cb39f-537">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-539">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="cb39f-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cb39f-540">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="cb39f-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb39f-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb39f-541">Az.EventGrid</span></span>
* <span data-ttu-id="cb39f-542">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cb39f-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cb39f-543">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cb39f-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cb39f-544">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="cb39f-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb39f-545">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="cb39f-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb39f-546">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="cb39f-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb39f-547">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="cb39f-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cb39f-548">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="cb39f-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb39f-549">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="cb39f-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb39f-550">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="cb39f-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb39f-551">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="cb39f-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="cb39f-552">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cb39f-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cb39f-553">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="cb39f-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb39f-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-554">Az.IotHub</span></span>
* <span data-ttu-id="cb39f-555">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="cb39f-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb39f-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb39f-556">Az.LogicApp</span></span>
* <span data-ttu-id="cb39f-557">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="cb39f-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-558">Az.Resources</span></span>
* <span data-ttu-id="cb39f-559">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="cb39f-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cb39f-560">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cb39f-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cb39f-561">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb39f-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb39f-562">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="cb39f-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cb39f-563">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="cb39f-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cb39f-564">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cb39f-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb39f-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb39f-565">Az.SignalR</span></span>
* <span data-ttu-id="cb39f-566">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-567">Az.Sql</span></span>
* <span data-ttu-id="cb39f-568">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="cb39f-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb39f-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-569">Az.Storage</span></span>
* <span data-ttu-id="cb39f-570">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="cb39f-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cb39f-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb39f-571">New-AzStorageContext</span></span>
* <span data-ttu-id="cb39f-572">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="cb39f-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cb39f-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb39f-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-574">Az.Websites</span></span>
* <span data-ttu-id="cb39f-575">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="cb39f-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb39f-576">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cb39f-577">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cb39f-578">Geral</span><span class="sxs-lookup"><span data-stu-id="cb39f-578">General</span></span>

- <span data-ttu-id="cb39f-579">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="cb39f-579">General Availability of Az Module</span></span>
- <span data-ttu-id="cb39f-580">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="cb39f-580">Online help for each module</span></span>
- <span data-ttu-id="cb39f-581">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cb39f-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cb39f-582">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="cb39f-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cb39f-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-583">Az.Accounts</span></span>
- <span data-ttu-id="cb39f-584">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb39f-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="cb39f-585">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="cb39f-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb39f-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb39f-586">Az.ApiManagement</span></span>
- <span data-ttu-id="cb39f-587">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="cb39f-587">Fixes for #7002</span></span>
- <span data-ttu-id="cb39f-588">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cb39f-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb39f-589">Az.Batch</span></span>
- <span data-ttu-id="cb39f-590">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="cb39f-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cb39f-591">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="cb39f-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cb39f-592">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cb39f-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb39f-593">Az.Billing</span></span>
- <span data-ttu-id="cb39f-594">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cb39f-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-595">Az.CognitivServices</span></span>
- <span data-ttu-id="cb39f-596">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cb39f-597">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="cb39f-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb39f-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="cb39f-599">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb39f-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cb39f-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cb39f-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cb39f-601">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="cb39f-603">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cb39f-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb39f-604">Az.Monitor</span></span>
- <span data-ttu-id="cb39f-605">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cb39f-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb39f-606">Az.KeyVault</span></span>
- <span data-ttu-id="cb39f-607">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="cb39f-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cb39f-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb39f-608">Az.MachineLearning</span></span>
- <span data-ttu-id="cb39f-609">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cb39f-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cb39f-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb39f-610">Az.Media</span></span>
- <span data-ttu-id="cb39f-611">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cb39f-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb39f-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-612">Az.Network</span></span>
<span data-ttu-id="cb39f-613">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="cb39f-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cb39f-614">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="cb39f-614">New cmdlets added:</span></span>
        - <span data-ttu-id="cb39f-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cb39f-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cb39f-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb39f-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cb39f-623">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb39f-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cb39f-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb39f-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cb39f-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb39f-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb39f-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb39f-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cb39f-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cb39f-629">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="cb39f-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cb39f-630">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cb39f-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cb39f-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb39f-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb39f-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb39f-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb39f-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb39f-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cb39f-634">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb39f-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cb39f-635">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cb39f-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb39f-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="cb39f-637">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cb39f-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb39f-638">Az.Profile</span></span>
- <span data-ttu-id="cb39f-639">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb39f-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="cb39f-641">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cb39f-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-642">Az.Resources</span></span>
- <span data-ttu-id="cb39f-643">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb39f-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb39f-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="cb39f-645">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="cb39f-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cb39f-646">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cb39f-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb39f-647">Az.SIgnalR</span></span>
- <span data-ttu-id="cb39f-648">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb39f-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cb39f-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-649">Az.Sql</span></span>
- <span data-ttu-id="cb39f-650">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="cb39f-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cb39f-651">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="cb39f-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cb39f-652">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb39f-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-653">Az.Storage</span></span>
- <span data-ttu-id="cb39f-654">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb39f-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-655">Az.Websites</span></span>
- <span data-ttu-id="cb39f-656">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="cb39f-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cb39f-657">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cb39f-658">Geral</span><span class="sxs-lookup"><span data-stu-id="cb39f-658">General</span></span>

* <span data-ttu-id="cb39f-659">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="cb39f-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb39f-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-660">Az.Compute</span></span>

* <span data-ttu-id="cb39f-661">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="cb39f-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="cb39f-663">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="cb39f-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cb39f-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb39f-664">Az.FrontDoor</span></span>

* <span data-ttu-id="cb39f-665">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="cb39f-665">Fixed some broken links</span></span>
    - <span data-ttu-id="cb39f-666">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cb39f-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cb39f-667">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="cb39f-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb39f-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="cb39f-669">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cb39f-670">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="cb39f-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb39f-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-671">Az.Resources</span></span>

* <span data-ttu-id="cb39f-672">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cb39f-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cb39f-673">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="cb39f-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cb39f-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-674">Az.Sql</span></span>

* <span data-ttu-id="cb39f-675">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="cb39f-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cb39f-676">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="cb39f-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cb39f-677">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="cb39f-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb39f-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-678">Az.Storage</span></span>

* <span data-ttu-id="cb39f-679">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cb39f-680">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="cb39f-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cb39f-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb39f-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb39f-682">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="cb39f-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="cb39f-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb39f-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cb39f-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb39f-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb39f-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-685">Az.Websites</span></span>

* <span data-ttu-id="cb39f-686">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb39f-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="cb39f-687">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="cb39f-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cb39f-688">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb39f-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cb39f-689">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb39f-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb39f-690">Az.ApiManagement</span></span>
* <span data-ttu-id="cb39f-691">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="cb39f-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cb39f-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb39f-692">Az.Automation</span></span>
* <span data-ttu-id="cb39f-693">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="cb39f-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb39f-694">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="cb39f-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cb39f-695">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="cb39f-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cb39f-696">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="cb39f-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cb39f-697">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="cb39f-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb39f-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-698">Az.Compute</span></span>
* <span data-ttu-id="cb39f-699">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="cb39f-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cb39f-700">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="cb39f-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb39f-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb39f-702">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="cb39f-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cb39f-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb39f-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb39f-704">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="cb39f-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb39f-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-705">Az.Network</span></span>
* <span data-ttu-id="cb39f-706">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="cb39f-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cb39f-707">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="cb39f-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cb39f-708">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="cb39f-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="cb39f-709">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb39f-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cb39f-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cb39f-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cb39f-711">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="cb39f-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cb39f-712">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb39f-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cb39f-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cb39f-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cb39f-714">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb39f-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cb39f-715">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="cb39f-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cb39f-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb39f-716">Az.Relay</span></span>
* <span data-ttu-id="cb39f-717">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="cb39f-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb39f-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-718">Az.Resources</span></span>
* <span data-ttu-id="cb39f-719">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="cb39f-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cb39f-720">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="cb39f-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cb39f-721">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cb39f-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb39f-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb39f-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb39f-723">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="cb39f-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cb39f-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-724">Az.Sql</span></span>
* <span data-ttu-id="cb39f-725">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="cb39f-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cb39f-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb39f-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb39f-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb39f-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb39f-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb39f-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb39f-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb39f-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb39f-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb39f-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb39f-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb39f-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb39f-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cb39f-734">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cb39f-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cb39f-735">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="cb39f-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cb39f-736">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="cb39f-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cb39f-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb39f-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb39f-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb39f-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb39f-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb39f-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cb39f-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cb39f-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cb39f-741">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="cb39f-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cb39f-742">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cb39f-743">Geral</span><span class="sxs-lookup"><span data-stu-id="cb39f-743">General</span></span>
* <span data-ttu-id="cb39f-744">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="cb39f-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cb39f-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb39f-745">Az.Profile</span></span>
* <span data-ttu-id="cb39f-746">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb39f-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cb39f-747">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="cb39f-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cb39f-748">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cb39f-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cb39f-749">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="cb39f-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cb39f-750">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="cb39f-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cb39f-751">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="cb39f-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cb39f-752">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="cb39f-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb39f-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb39f-754">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cb39f-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-755">Az.Compute</span></span>
* <span data-ttu-id="cb39f-756">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cb39f-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cb39f-757">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cb39f-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cb39f-758">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="cb39f-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-760">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="cb39f-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cb39f-761">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="cb39f-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cb39f-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cb39f-762">Az.Insights</span></span>
* <span data-ttu-id="cb39f-763">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="cb39f-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cb39f-764">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="cb39f-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cb39f-765">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="cb39f-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cb39f-766">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="cb39f-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-767">Az.Network</span></span>
* <span data-ttu-id="cb39f-768">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="cb39f-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cb39f-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb39f-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cb39f-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cb39f-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cb39f-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb39f-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cb39f-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cb39f-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cb39f-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb39f-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cb39f-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb39f-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb39f-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb39f-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb39f-776">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="cb39f-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-777">Az.Resources</span></span>
* <span data-ttu-id="cb39f-778">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cb39f-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cb39f-779">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="cb39f-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb39f-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb39f-780">Az.ServiceBus</span></span>
* <span data-ttu-id="cb39f-781">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="cb39f-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb39f-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb39f-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb39f-783">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="cb39f-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cb39f-784">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="cb39f-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cb39f-785">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cb39f-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cb39f-786">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cb39f-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cb39f-787">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="cb39f-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cb39f-788">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cb39f-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb39f-789">Az.Profile</span></span>
* <span data-ttu-id="cb39f-790">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="cb39f-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cb39f-791">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb39f-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-792">Az.Compute</span></span>
* <span data-ttu-id="cb39f-793">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="cb39f-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cb39f-794">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="cb39f-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb39f-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb39f-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb39f-796">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="cb39f-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cb39f-797">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb39f-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cb39f-798">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="cb39f-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb39f-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="cb39f-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb39f-800">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb39f-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-801">Az.Network</span></span>
* <span data-ttu-id="cb39f-802">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="cb39f-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cb39f-803">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="cb39f-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-804">Az.Resources</span></span>
* <span data-ttu-id="cb39f-805">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="cb39f-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cb39f-806">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="cb39f-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cb39f-807">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cb39f-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cb39f-808">Azure.Storage</span></span>
* <span data-ttu-id="cb39f-809">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="cb39f-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cb39f-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb39f-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cb39f-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb39f-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb39f-812">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="cb39f-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cb39f-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cb39f-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="cb39f-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb39f-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb39f-815">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="cb39f-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb39f-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb39f-816">Az.Compute</span></span>
* <span data-ttu-id="cb39f-817">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="cb39f-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cb39f-818">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cb39f-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cb39f-819">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="cb39f-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cb39f-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cb39f-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cb39f-821">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="cb39f-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb39f-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb39f-822">Az.Network</span></span>
* <span data-ttu-id="cb39f-823">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="cb39f-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cb39f-824">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="cb39f-824">new cmdlets added</span></span>
    - <span data-ttu-id="cb39f-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb39f-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb39f-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb39f-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb39f-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb39f-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb39f-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb39f-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb39f-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cb39f-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cb39f-831">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="cb39f-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cb39f-832">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="cb39f-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cb39f-833">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="cb39f-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb39f-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb39f-834">Az.RedisCache</span></span>
* <span data-ttu-id="cb39f-835">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="cb39f-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cb39f-836">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="cb39f-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb39f-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb39f-837">Az.Resources</span></span>
* <span data-ttu-id="cb39f-838">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb39f-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb39f-839">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="cb39f-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb39f-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb39f-840">Az.Sql</span></span>
* <span data-ttu-id="cb39f-841">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="cb39f-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb39f-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb39f-842">Az.Websites</span></span>
* <span data-ttu-id="cb39f-843">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="cb39f-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cb39f-844">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="cb39f-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cb39f-845">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="cb39f-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cb39f-846">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="cb39f-846">Initial Release</span></span>