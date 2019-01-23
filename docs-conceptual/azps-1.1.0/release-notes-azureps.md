---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341857"
---
## <a name="110---january-2019"></a><span data-ttu-id="65250-101">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="65250-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="65250-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-102">Az.Accounts</span></span>
* <span data-ttu-id="65250-103">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="65250-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="65250-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-104">Az.Compute</span></span>
* <span data-ttu-id="65250-105">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="65250-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="65250-106">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="65250-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="65250-107">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="65250-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65250-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="65250-109">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="65250-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="65250-110">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="65250-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="65250-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="65250-111">Az.EventGrid</span></span>
* <span data-ttu-id="65250-112">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="65250-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="65250-113">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="65250-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="65250-114">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="65250-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="65250-115">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="65250-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="65250-116">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="65250-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="65250-117">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="65250-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="65250-118">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="65250-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="65250-119">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="65250-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="65250-120">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="65250-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="65250-121">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="65250-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="65250-122">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="65250-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="65250-123">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="65250-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="65250-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="65250-124">Az.IotHub</span></span>
* <span data-ttu-id="65250-125">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="65250-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="65250-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="65250-126">Az.LogicApp</span></span>
* <span data-ttu-id="65250-127">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="65250-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="65250-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-128">Az.Resources</span></span>
* <span data-ttu-id="65250-129">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="65250-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="65250-130">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="65250-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="65250-131">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="65250-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="65250-132">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="65250-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="65250-133">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="65250-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="65250-134">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="65250-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="65250-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="65250-135">Az.SignalR</span></span>
* <span data-ttu-id="65250-136">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="65250-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="65250-137">Az.Sql</span></span>
* <span data-ttu-id="65250-138">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="65250-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="65250-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="65250-139">Az.Storage</span></span>
* <span data-ttu-id="65250-140">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="65250-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="65250-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="65250-141">New-AzStorageContext</span></span>
* <span data-ttu-id="65250-142">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="65250-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="65250-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="65250-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="65250-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="65250-144">Az.Websites</span></span>
* <span data-ttu-id="65250-145">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="65250-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="65250-146">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="65250-147">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="65250-148">Geral</span><span class="sxs-lookup"><span data-stu-id="65250-148">General</span></span>

- <span data-ttu-id="65250-149">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="65250-149">General Availability of Az Module</span></span>
- <span data-ttu-id="65250-150">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="65250-150">Online help for each module</span></span>
- <span data-ttu-id="65250-151">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="65250-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="65250-152">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="65250-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="65250-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-153">Az.Accounts</span></span>
- <span data-ttu-id="65250-154">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="65250-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="65250-155">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="65250-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="65250-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="65250-156">Az.ApiManagement</span></span>
- <span data-ttu-id="65250-157">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="65250-157">Fixes for #7002</span></span>
- <span data-ttu-id="65250-158">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="65250-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="65250-159">Az.Batch</span></span>
- <span data-ttu-id="65250-160">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="65250-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="65250-161">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="65250-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="65250-162">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="65250-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="65250-163">Az.Billing</span></span>
- <span data-ttu-id="65250-164">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="65250-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="65250-165">Az.CognitivServices</span></span>
- <span data-ttu-id="65250-166">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="65250-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="65250-167">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="65250-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="65250-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="65250-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="65250-169">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="65250-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="65250-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="65250-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="65250-171">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="65250-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65250-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="65250-173">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="65250-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="65250-174">Az.Monitor</span></span>
- <span data-ttu-id="65250-175">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="65250-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="65250-176">Az.KeyVault</span></span>
- <span data-ttu-id="65250-177">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="65250-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="65250-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="65250-178">Az.MachineLearning</span></span>
- <span data-ttu-id="65250-179">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="65250-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="65250-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="65250-180">Az.Media</span></span>
- <span data-ttu-id="65250-181">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="65250-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="65250-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="65250-182">Az.Network</span></span>
<span data-ttu-id="65250-183">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="65250-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="65250-184">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="65250-184">New cmdlets added:</span></span>
        - <span data-ttu-id="65250-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="65250-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="65250-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="65250-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="65250-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="65250-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="65250-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="65250-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="65250-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="65250-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="65250-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="65250-193">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65250-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="65250-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65250-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="65250-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="65250-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="65250-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="65250-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="65250-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65250-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="65250-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="65250-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="65250-199">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="65250-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="65250-200">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="65250-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="65250-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65250-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="65250-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65250-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="65250-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65250-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="65250-204">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="65250-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="65250-205">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="65250-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="65250-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="65250-207">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="65250-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="65250-208">Az.Profile</span></span>
- <span data-ttu-id="65250-209">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="65250-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="65250-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="65250-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="65250-211">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="65250-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-212">Az.Resources</span></span>
- <span data-ttu-id="65250-213">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="65250-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="65250-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="65250-215">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="65250-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="65250-216">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="65250-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="65250-217">Az.SIgnalR</span></span>
- <span data-ttu-id="65250-218">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="65250-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="65250-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="65250-219">Az.Sql</span></span>
- <span data-ttu-id="65250-220">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="65250-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="65250-221">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="65250-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="65250-222">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="65250-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="65250-223">Az.Storage</span></span>
- <span data-ttu-id="65250-224">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="65250-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="65250-225">Az.Websites</span></span>
- <span data-ttu-id="65250-226">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="65250-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="65250-227">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="65250-228">Geral</span><span class="sxs-lookup"><span data-stu-id="65250-228">General</span></span>

* <span data-ttu-id="65250-229">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="65250-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="65250-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-230">Az.Compute</span></span>

* <span data-ttu-id="65250-231">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="65250-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="65250-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65250-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="65250-233">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="65250-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="65250-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="65250-234">Az.FrontDoor</span></span>

* <span data-ttu-id="65250-235">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="65250-235">Fixed some broken links</span></span>
    - <span data-ttu-id="65250-236">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="65250-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="65250-237">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="65250-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="65250-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="65250-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="65250-239">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="65250-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="65250-240">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="65250-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="65250-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-241">Az.Resources</span></span>

* <span data-ttu-id="65250-242">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="65250-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="65250-243">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="65250-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="65250-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="65250-244">Az.Sql</span></span>

* <span data-ttu-id="65250-245">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="65250-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="65250-246">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="65250-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="65250-247">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="65250-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="65250-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="65250-248">Az.Storage</span></span>

* <span data-ttu-id="65250-249">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65250-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="65250-250">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="65250-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="65250-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="65250-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="65250-252">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="65250-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="65250-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="65250-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="65250-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="65250-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="65250-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="65250-255">Az.Websites</span></span>

* <span data-ttu-id="65250-256">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="65250-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="65250-257">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="65250-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="65250-258">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="65250-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="65250-259">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="65250-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="65250-260">Az.ApiManagement</span></span>
* <span data-ttu-id="65250-261">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="65250-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="65250-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="65250-262">Az.Automation</span></span>
* <span data-ttu-id="65250-263">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="65250-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="65250-264">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="65250-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="65250-265">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="65250-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="65250-266">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="65250-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="65250-267">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="65250-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="65250-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-268">Az.Compute</span></span>
* <span data-ttu-id="65250-269">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="65250-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="65250-270">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="65250-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="65250-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="65250-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="65250-272">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="65250-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="65250-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="65250-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="65250-274">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="65250-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="65250-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="65250-275">Az.Network</span></span>
* <span data-ttu-id="65250-276">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="65250-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="65250-277">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="65250-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="65250-278">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="65250-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="65250-279">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="65250-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="65250-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="65250-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="65250-281">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="65250-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="65250-282">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="65250-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="65250-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="65250-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="65250-284">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="65250-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="65250-285">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="65250-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="65250-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="65250-286">Az.Relay</span></span>
* <span data-ttu-id="65250-287">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="65250-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="65250-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-288">Az.Resources</span></span>
* <span data-ttu-id="65250-289">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="65250-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="65250-290">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="65250-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="65250-291">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="65250-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="65250-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="65250-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="65250-293">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="65250-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="65250-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="65250-294">Az.Sql</span></span>
* <span data-ttu-id="65250-295">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="65250-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="65250-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="65250-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="65250-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="65250-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="65250-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="65250-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="65250-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="65250-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="65250-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="65250-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="65250-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="65250-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="65250-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="65250-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="65250-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="65250-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="65250-304">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65250-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="65250-305">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="65250-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="65250-306">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="65250-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="65250-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="65250-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="65250-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="65250-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="65250-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="65250-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="65250-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="65250-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="65250-311">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="65250-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="65250-312">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="65250-313">Geral</span><span class="sxs-lookup"><span data-stu-id="65250-313">General</span></span>
* <span data-ttu-id="65250-314">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="65250-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="65250-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="65250-315">Az.Profile</span></span>
* <span data-ttu-id="65250-316">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="65250-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="65250-317">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="65250-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="65250-318">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="65250-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="65250-319">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="65250-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="65250-320">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="65250-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="65250-321">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="65250-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="65250-322">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="65250-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="65250-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="65250-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="65250-324">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="65250-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="65250-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-325">Az.Compute</span></span>
* <span data-ttu-id="65250-326">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="65250-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="65250-327">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="65250-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="65250-328">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="65250-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="65250-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65250-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="65250-330">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="65250-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="65250-331">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="65250-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="65250-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="65250-332">Az.Insights</span></span>
* <span data-ttu-id="65250-333">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="65250-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="65250-334">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="65250-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="65250-335">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="65250-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="65250-336">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="65250-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="65250-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="65250-337">Az.Network</span></span>
* <span data-ttu-id="65250-338">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="65250-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="65250-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="65250-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="65250-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="65250-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="65250-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="65250-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="65250-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="65250-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="65250-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="65250-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="65250-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="65250-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="65250-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="65250-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="65250-346">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="65250-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="65250-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-347">Az.Resources</span></span>
* <span data-ttu-id="65250-348">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="65250-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="65250-349">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="65250-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="65250-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="65250-350">Az.ServiceBus</span></span>
* <span data-ttu-id="65250-351">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="65250-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="65250-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="65250-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="65250-353">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="65250-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="65250-354">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="65250-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="65250-355">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="65250-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="65250-356">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="65250-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="65250-357">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="65250-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="65250-358">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="65250-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="65250-359">Az.Profile</span></span>
* <span data-ttu-id="65250-360">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="65250-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="65250-361">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="65250-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="65250-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-362">Az.Compute</span></span>
* <span data-ttu-id="65250-363">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="65250-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="65250-364">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="65250-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="65250-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65250-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="65250-366">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="65250-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="65250-367">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="65250-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="65250-368">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="65250-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="65250-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="65250-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="65250-370">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="65250-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="65250-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="65250-371">Az.Network</span></span>
* <span data-ttu-id="65250-372">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="65250-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="65250-373">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="65250-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="65250-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-374">Az.Resources</span></span>
* <span data-ttu-id="65250-375">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="65250-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="65250-376">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="65250-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="65250-377">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="65250-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="65250-378">Azure.Storage</span></span>
* <span data-ttu-id="65250-379">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="65250-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="65250-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="65250-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="65250-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="65250-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="65250-382">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="65250-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="65250-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="65250-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="65250-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="65250-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="65250-385">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="65250-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="65250-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="65250-386">Az.Compute</span></span>
* <span data-ttu-id="65250-387">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="65250-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="65250-388">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="65250-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="65250-389">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="65250-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="65250-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="65250-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="65250-391">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="65250-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="65250-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="65250-392">Az.Network</span></span>
* <span data-ttu-id="65250-393">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="65250-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="65250-394">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="65250-394">new cmdlets added</span></span>
    - <span data-ttu-id="65250-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65250-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="65250-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65250-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="65250-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65250-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="65250-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="65250-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="65250-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="65250-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="65250-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="65250-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="65250-401">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="65250-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="65250-402">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="65250-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="65250-403">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="65250-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="65250-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="65250-404">Az.RedisCache</span></span>
* <span data-ttu-id="65250-405">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="65250-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="65250-406">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="65250-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="65250-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="65250-407">Az.Resources</span></span>
* <span data-ttu-id="65250-408">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="65250-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="65250-409">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="65250-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="65250-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="65250-410">Az.Sql</span></span>
* <span data-ttu-id="65250-411">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="65250-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="65250-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="65250-412">Az.Websites</span></span>
* <span data-ttu-id="65250-413">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="65250-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="65250-414">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="65250-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="65250-415">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="65250-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="65250-416">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="65250-416">Initial Release</span></span>