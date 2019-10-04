---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319323"
---
## <a name="270---september-2019"></a><span data-ttu-id="4fcd3-103">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-104">Az.ApiManagement</span></span>
* <span data-ttu-id="4fcd3-105">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4fcd3-106">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4fcd3-107">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-108">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-109">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4fcd3-110">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="4fcd3-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4fcd3-111">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-112">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-113">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4fcd3-114">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4fcd3-115">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4fcd3-116">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4fcd3-117">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4fcd3-118">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4fcd3-119">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4fcd3-120">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4fcd3-121">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-122">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-123">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4fcd3-124">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="4fcd3-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4fcd3-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4fcd3-125">Az.HDInsight</span></span>
* <span data-ttu-id="4fcd3-126">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="4fcd3-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4fcd3-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-127">Az.IotHub</span></span>
* <span data-ttu-id="4fcd3-128">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4fcd3-129">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4fcd3-130">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-130">New cmdlets are:</span></span>
    - <span data-ttu-id="4fcd3-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4fcd3-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4fcd3-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4fcd3-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4fcd3-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4fcd3-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4fcd3-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4fcd3-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-135">Az.Monitor</span></span>
* <span data-ttu-id="4fcd3-136">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4fcd3-137">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4fcd3-138">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4fcd3-139">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4fcd3-140">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4fcd3-141">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4fcd3-142">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4fcd3-143">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4fcd3-144">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4fcd3-145">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4fcd3-146">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4fcd3-147">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4fcd3-148">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4fcd3-149">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4fcd3-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4fcd3-150">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4fcd3-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4fcd3-151">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4fcd3-152">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4fcd3-153">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4fcd3-154">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4fcd3-155">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-155">Overall improved help files</span></span>
* <span data-ttu-id="4fcd3-156">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-157">Az.Network</span></span>
* <span data-ttu-id="4fcd3-158">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="4fcd3-159">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="4fcd3-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4fcd3-160">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="4fcd3-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4fcd3-161">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4fcd3-162">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="4fcd3-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4fcd3-163">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="4fcd3-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4fcd3-164">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4fcd3-165">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4fcd3-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4fcd3-166">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4fcd3-167">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4fcd3-168">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4fcd3-169">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="4fcd3-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4fcd3-170">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-170">New cmdlets</span></span>
        - <span data-ttu-id="4fcd3-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4fcd3-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4fcd3-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4fcd3-173">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="4fcd3-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4fcd3-174">New-VpnSite</span></span>
        - <span data-ttu-id="4fcd3-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4fcd3-175">Update-VpnSite</span></span>
        - <span data-ttu-id="4fcd3-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-176">New-VpnConnection</span></span>
        - <span data-ttu-id="4fcd3-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-177">Update-VpnConnection</span></span>
* <span data-ttu-id="4fcd3-178">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-180">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4fcd3-181">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="4fcd3-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-182">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-183">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-185">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4fcd3-186">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4fcd3-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4fcd3-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4fcd3-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4fcd3-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4fcd3-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4fcd3-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4fcd3-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4fcd3-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4fcd3-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4fcd3-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4fcd3-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4fcd3-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4fcd3-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4fcd3-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4fcd3-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4fcd3-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4fcd3-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4fcd3-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4fcd3-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4fcd3-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4fcd3-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4fcd3-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4fcd3-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4fcd3-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4fcd3-200">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4fcd3-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-201">Az.SignalR</span></span>
* <span data-ttu-id="4fcd3-202">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-203">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-204">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4fcd3-205">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4fcd3-206">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4fcd3-207">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4fcd3-208">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-209">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-210">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4fcd3-211">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="4fcd3-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4fcd3-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4fcd3-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4fcd3-214">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4fcd3-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4fcd3-216">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4fcd3-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4fcd3-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fcd3-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4fcd3-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fcd3-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4fcd3-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fcd3-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4fcd3-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fcd3-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-221">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-222">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="4fcd3-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4fcd3-223">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="4fcd3-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4fcd3-224">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4fcd3-225">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4fcd3-226">Geral</span><span class="sxs-lookup"><span data-stu-id="4fcd3-226">General</span></span>
* <span data-ttu-id="4fcd3-227">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-228">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-229">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4fcd3-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4fcd3-230">Az.Aks</span></span>
* <span data-ttu-id="4fcd3-231">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4fcd3-232">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4fcd3-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-233">Az.ApiManagement</span></span>
* <span data-ttu-id="4fcd3-234">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4fcd3-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4fcd3-235">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="4fcd3-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4fcd3-236">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4fcd3-237">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4fcd3-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4fcd3-238">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4fcd3-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4fcd3-239">Az.Batch</span></span>
* <span data-ttu-id="4fcd3-240">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="4fcd3-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4fcd3-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4fcd3-241">Az.Cdn</span></span>
* <span data-ttu-id="4fcd3-242">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="4fcd3-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-243">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-244">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4fcd3-245">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fcd3-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4fcd3-246">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4fcd3-247">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4fcd3-248">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4fcd3-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4fcd3-249">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4fcd3-250">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4fcd3-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4fcd3-251">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-252">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-253">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4fcd3-254">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="4fcd3-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4fcd3-255">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4fcd3-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4fcd3-256">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="4fcd3-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-258">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4fcd3-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-259">Az.EventHub</span></span>
* <span data-ttu-id="4fcd3-260">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4fcd3-261">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="4fcd3-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4fcd3-262">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4fcd3-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4fcd3-263">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4fcd3-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4fcd3-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4fcd3-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4fcd3-265">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-266">Az.Monitor</span></span>
* <span data-ttu-id="4fcd3-267">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-268">Az.Network</span></span>
* <span data-ttu-id="4fcd3-269">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4fcd3-270">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4fcd3-271">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4fcd3-272">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="4fcd3-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4fcd3-273">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="4fcd3-274">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4fcd3-275">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4fcd3-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-277">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4fcd3-278">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-278">Added example</span></span>
    - <span data-ttu-id="4fcd3-279">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4fcd3-280">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4fcd3-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4fcd3-281">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4fcd3-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-283">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-284">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-285">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="4fcd3-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4fcd3-286">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="4fcd3-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4fcd3-287">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4fcd3-288">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-289">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-290">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4fcd3-291">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4fcd3-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4fcd3-292">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="4fcd3-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-294">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4fcd3-295">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4fcd3-296">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4fcd3-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4fcd3-297">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4fcd3-298">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4fcd3-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4fcd3-299">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4fcd3-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-300">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-301">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-302">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-303">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fcd3-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4fcd3-304">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="4fcd3-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4fcd3-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4fcd3-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4fcd3-307">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="4fcd3-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4fcd3-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-309">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-310">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4fcd3-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4fcd3-311">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-312">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-313">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4fcd3-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4fcd3-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4fcd3-315">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-316">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-317">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-319">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-320">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-321">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4fcd3-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4fcd3-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4fcd3-323">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4fcd3-324">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4fcd3-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-325">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-326">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4fcd3-327">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="4fcd3-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4fcd3-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-328">Az.EventHub</span></span>
* <span data-ttu-id="4fcd3-329">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4fcd3-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4fcd3-330">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4fcd3-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-331">Az.KeyVault</span></span>
* <span data-ttu-id="4fcd3-332">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4fcd3-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-333">Az.LogicApp</span></span>
* <span data-ttu-id="4fcd3-334">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="4fcd3-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4fcd3-335">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="4fcd3-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4fcd3-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-336">Az.ManagedServices</span></span>
* <span data-ttu-id="4fcd3-337">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-338">Az.Network</span></span>
* <span data-ttu-id="4fcd3-339">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4fcd3-340">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-340">New cmdlets</span></span>
        - <span data-ttu-id="4fcd3-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fcd3-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4fcd3-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4fcd3-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4fcd3-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4fcd3-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4fcd3-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4fcd3-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4fcd3-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4fcd3-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4fcd3-349">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="4fcd3-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4fcd3-350">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4fcd3-351">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4fcd3-352">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4fcd3-353">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4fcd3-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4fcd3-354">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4fcd3-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4fcd3-355">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-355">Updated cmdlets</span></span>
        - <span data-ttu-id="4fcd3-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4fcd3-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4fcd3-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4fcd3-359">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4fcd3-360">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4fcd3-361">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="4fcd3-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4fcd3-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4fcd3-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4fcd3-365">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4fcd3-366">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4fcd3-367">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-369">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="4fcd3-370">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="4fcd3-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-372">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4fcd3-373">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4fcd3-374">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4fcd3-375">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4fcd3-376">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4fcd3-377">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4fcd3-378">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4fcd3-379">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4fcd3-380">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4fcd3-381">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-382">Az.Resources</span></span>
- <span data-ttu-id="4fcd3-383">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4fcd3-384">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4fcd3-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-385">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-386">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4fcd3-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4fcd3-387">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4fcd3-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-388">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-389">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4fcd3-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4fcd3-390">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="4fcd3-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4fcd3-391">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-392">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-393">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4fcd3-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4fcd3-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4fcd3-394">Az.StorageSync</span></span>
* <span data-ttu-id="4fcd3-395">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4fcd3-396">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4fcd3-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-397">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-398">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4fcd3-399">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4fcd3-400">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4fcd3-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4fcd3-401">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-402">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-403">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="4fcd3-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4fcd3-404">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4fcd3-405">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4fcd3-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4fcd3-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-406">Az.Advisor</span></span>
* <span data-ttu-id="4fcd3-407">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4fcd3-408">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-409">Az.ApiManagement</span></span>
* <span data-ttu-id="4fcd3-410">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4fcd3-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4fcd3-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4fcd3-412">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="4fcd3-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4fcd3-413">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4fcd3-414">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4fcd3-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4fcd3-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4fcd3-416">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="4fcd3-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-417">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-418">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-419">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-420">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-421">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-422">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4fcd3-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4fcd3-423">Az.EventGrid</span></span>
* <span data-ttu-id="4fcd3-424">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4fcd3-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-425">Az.IotHub</span></span>
* <span data-ttu-id="4fcd3-426">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-427">Az.Network</span></span>
* <span data-ttu-id="4fcd3-428">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="4fcd3-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4fcd3-429">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4fcd3-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="4fcd3-431">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4fcd3-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4fcd3-432">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4fcd3-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-434">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4fcd3-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-436">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="4fcd3-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-437">Az.Resources</span></span>
    - <span data-ttu-id="4fcd3-438">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="4fcd3-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4fcd3-439">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4fcd3-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4fcd3-440">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="4fcd3-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4fcd3-441">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-442">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-443">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-444">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-445">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="4fcd3-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4fcd3-446">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4fcd3-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4fcd3-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4fcd3-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4fcd3-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4fcd3-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4fcd3-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4fcd3-453">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="4fcd3-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-454">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-455">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4fcd3-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4fcd3-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4fcd3-457">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4fcd3-458">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="4fcd3-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4fcd3-459">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4fcd3-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4fcd3-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4fcd3-462">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4fcd3-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4fcd3-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4fcd3-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4fcd3-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4fcd3-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4fcd3-465">Az.StorageSync</span></span>
* <span data-ttu-id="4fcd3-466">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4fcd3-467">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-468">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-469">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="4fcd3-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4fcd3-470">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4fcd3-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4fcd3-471">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="4fcd3-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4fcd3-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4fcd3-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4fcd3-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4fcd3-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-474">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-475">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4fcd3-476">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4fcd3-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4fcd3-477">Az.Dns</span></span>
* <span data-ttu-id="4fcd3-478">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4fcd3-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4fcd3-479">Az.EventGrid</span></span>
* <span data-ttu-id="4fcd3-480">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4fcd3-481">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-481">New cmdlets:</span></span>
    - <span data-ttu-id="4fcd3-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4fcd3-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4fcd3-483">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4fcd3-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4fcd3-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4fcd3-485">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4fcd3-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4fcd3-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4fcd3-487">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4fcd3-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4fcd3-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4fcd3-489">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4fcd3-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4fcd3-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4fcd3-491">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4fcd3-492">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4fcd3-493">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4fcd3-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4fcd3-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4fcd3-495">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="4fcd3-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="4fcd3-496">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4fcd3-497">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4fcd3-498">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="4fcd3-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4fcd3-500">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4fcd3-501">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4fcd3-502">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4fcd3-503">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4fcd3-504">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="4fcd3-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4fcd3-505">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4fcd3-506">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4fcd3-507">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="4fcd3-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="4fcd3-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4fcd3-509">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4fcd3-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4fcd3-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4fcd3-511">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4fcd3-512">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4fcd3-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-513">Az.FrontDoor</span></span>
* <span data-ttu-id="4fcd3-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4fcd3-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4fcd3-515">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4fcd3-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4fcd3-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4fcd3-517">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4fcd3-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-518">Az.Network</span></span>
* <span data-ttu-id="4fcd3-519">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4fcd3-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4fcd3-520">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-520">New cmdlets</span></span>
        - <span data-ttu-id="4fcd3-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4fcd3-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4fcd3-522">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4fcd3-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4fcd3-523">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-523">New cmdlets</span></span> 
        - <span data-ttu-id="4fcd3-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4fcd3-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4fcd3-525">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4fcd3-526">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-526">New cmdlets</span></span> 
        - <span data-ttu-id="4fcd3-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="4fcd3-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4fcd3-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4fcd3-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4fcd3-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4fcd3-532">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fcd3-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4fcd3-533">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-533">New cmdlets</span></span>
        - <span data-ttu-id="4fcd3-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fcd3-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4fcd3-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fcd3-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4fcd3-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4fcd3-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4fcd3-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4fcd3-538">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4fcd3-539">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4fcd3-540">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4fcd3-541">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4fcd3-542">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4fcd3-543">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4fcd3-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4fcd3-544">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4fcd3-545">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4fcd3-546">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4fcd3-547">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4fcd3-548">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4fcd3-549">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4fcd3-550">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4fcd3-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4fcd3-551">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4fcd3-552">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4fcd3-553">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4fcd3-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4fcd3-554">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4fcd3-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4fcd3-555">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4fcd3-556">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4fcd3-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="4fcd3-557">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="4fcd3-558">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4fcd3-559">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4fcd3-560">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-562">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-563">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-564">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4fcd3-565">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4fcd3-566">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4fcd3-567">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-569">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-570">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-571">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4fcd3-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4fcd3-572">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4fcd3-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4fcd3-573">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4fcd3-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4fcd3-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4fcd3-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4fcd3-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4fcd3-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4fcd3-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4fcd3-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4fcd3-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4fcd3-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4fcd3-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-579">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-580">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4fcd3-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4fcd3-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="4fcd3-582">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="4fcd3-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4fcd3-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-584">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-585">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="4fcd3-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4fcd3-586">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fcd3-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4fcd3-587">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4fcd3-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4fcd3-588">Az.Cdn</span></span>
* <span data-ttu-id="4fcd3-589">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-590">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-591">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4fcd3-592">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4fcd3-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-593">Az.EventHub</span></span>
* <span data-ttu-id="4fcd3-594">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4fcd3-595">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcd3-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-596">Az.Network</span></span>
* <span data-ttu-id="4fcd3-597">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="4fcd3-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4fcd3-598">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="4fcd3-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4fcd3-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="4fcd3-600">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-602">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="4fcd3-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-603">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-604">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fcd3-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-606">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4fcd3-607">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-608">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-609">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4fcd3-610">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4fcd3-611">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4fcd3-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4fcd3-612">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-613">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-614">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4fcd3-615">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-616">Az.ApiManagement</span></span>
* <span data-ttu-id="4fcd3-617">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4fcd3-618">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4fcd3-619">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4fcd3-620">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4fcd3-621">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4fcd3-622">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4fcd3-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4fcd3-623">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4fcd3-624">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4fcd3-625">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4fcd3-626">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="4fcd3-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4fcd3-627">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4fcd3-628">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="4fcd3-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4fcd3-629">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="4fcd3-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4fcd3-630">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4fcd3-631">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4fcd3-632">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4fcd3-633">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4fcd3-634">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4fcd3-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4fcd3-635">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="4fcd3-636">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="4fcd3-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4fcd3-637">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="4fcd3-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4fcd3-638">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4fcd3-639">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4fcd3-640">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="4fcd3-641">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4fcd3-642">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4fcd3-643">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4fcd3-644">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4fcd3-645">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4fcd3-646">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4fcd3-647">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="4fcd3-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4fcd3-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4fcd3-649">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4fcd3-650">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4fcd3-651">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4fcd3-652">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="4fcd3-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4fcd3-653">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4fcd3-654">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4fcd3-655">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4fcd3-656">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="4fcd3-657">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4fcd3-658">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4fcd3-659">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4fcd3-660">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="4fcd3-661">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4fcd3-662">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4fcd3-663">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="4fcd3-664">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="4fcd3-665">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4fcd3-666">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4fcd3-667">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4fcd3-668">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4fcd3-669">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4fcd3-670">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4fcd3-671">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4fcd3-672">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4fcd3-673">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4fcd3-674">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4fcd3-675">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4fcd3-676">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4fcd3-677">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4fcd3-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4fcd3-678">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4fcd3-679">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4fcd3-680">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4fcd3-681">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4fcd3-682">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4fcd3-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4fcd3-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4fcd3-684">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4fcd3-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4fcd3-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4fcd3-686">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4fcd3-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4fcd3-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4fcd3-688">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4fcd3-689">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4fcd3-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4fcd3-691">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="4fcd3-692">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4fcd3-693">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-694">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-695">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4fcd3-696">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4fcd3-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4fcd3-697">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4fcd3-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4fcd3-698">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4fcd3-699">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4fcd3-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4fcd3-700">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4fcd3-701">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-702">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-703">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4fcd3-704">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-706">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-707">Az.Monitor</span></span>
* <span data-ttu-id="4fcd3-708">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-709">Az.Network</span></span>
* <span data-ttu-id="4fcd3-710">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4fcd3-711">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="4fcd3-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4fcd3-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4fcd3-713">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4fcd3-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-714">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-715">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-716">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-717">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="4fcd3-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4fcd3-718">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-719">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-720">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="4fcd3-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-722">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4fcd3-723">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-724">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-725">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4fcd3-726">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4fcd3-727">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4fcd3-728">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4fcd3-729">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4fcd3-730">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fcd3-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="4fcd3-731">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="4fcd3-731">Breaking changes</span></span>
    - <span data-ttu-id="4fcd3-732">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4fcd3-733">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4fcd3-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4fcd3-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="4fcd3-735">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4fcd3-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4fcd3-736">Az.Dns</span></span>
* <span data-ttu-id="4fcd3-737">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="4fcd3-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4fcd3-738">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4fcd3-739">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4fcd3-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-740">Az.FrontDoor</span></span>
* <span data-ttu-id="4fcd3-741">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4fcd3-742">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4fcd3-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4fcd3-743">Az.HDInsight</span></span>
* <span data-ttu-id="4fcd3-744">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4fcd3-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4fcd3-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4fcd3-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4fcd3-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4fcd3-747">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4fcd3-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4fcd3-748">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4fcd3-749">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4fcd3-750">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-751">Az.Monitor</span></span>
* <span data-ttu-id="4fcd3-752">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="4fcd3-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4fcd3-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4fcd3-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4fcd3-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4fcd3-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4fcd3-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4fcd3-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4fcd3-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4fcd3-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4fcd3-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4fcd3-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4fcd3-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4fcd3-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4fcd3-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4fcd3-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4fcd3-764">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4fcd3-765">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-766">Az.Network</span></span>
* <span data-ttu-id="4fcd3-767">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="4fcd3-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4fcd3-768">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4fcd3-768">New cmdlets</span></span>
        - <span data-ttu-id="4fcd3-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="4fcd3-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4fcd3-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4fcd3-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4fcd3-773">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-773">Updated cmdlets</span></span>
        - <span data-ttu-id="4fcd3-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4fcd3-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4fcd3-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4fcd3-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4fcd3-776">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4fcd3-777">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4fcd3-778">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4fcd3-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="4fcd3-780">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4fcd3-781">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4fcd3-782">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-784">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4fcd3-785">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4fcd3-786">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4fcd3-787">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4fcd3-788">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4fcd3-789">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4fcd3-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4fcd3-790">Az.Relay</span></span>
* <span data-ttu-id="4fcd3-791">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="4fcd3-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-792">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-793">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4fcd3-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-794">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-795">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="4fcd3-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4fcd3-796">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4fcd3-797">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4fcd3-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="4fcd3-799">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4fcd3-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4fcd3-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4fcd3-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-803">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-804">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4fcd3-805">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4fcd3-806">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4fcd3-807">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4fcd3-807">Highlights since the last major release</span></span>
* <span data-ttu-id="4fcd3-808">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-808">General availability of `Az` module</span></span>
* <span data-ttu-id="4fcd3-809">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4fcd3-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4fcd3-810">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4fcd3-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4fcd3-811">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4fcd3-812">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4fcd3-813">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4fcd3-814">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4fcd3-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-815">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-816">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="4fcd3-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4fcd3-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4fcd3-817">Az.Batch</span></span>
* <span data-ttu-id="4fcd3-818">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4fcd3-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4fcd3-819">Az.Cdn</span></span>
* <span data-ttu-id="4fcd3-820">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-822">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-823">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-824">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4fcd3-825">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-826">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4fcd3-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-827">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-828">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-830">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4fcd3-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4fcd3-831">Az.EventGrid</span></span>
* <span data-ttu-id="4fcd3-832">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4fcd3-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-833">Az.EventHub</span></span>
* <span data-ttu-id="4fcd3-834">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4fcd3-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="4fcd3-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4fcd3-835">Az.HDInsight</span></span>
* <span data-ttu-id="4fcd3-836">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4fcd3-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-837">Az.IotHub</span></span>
* <span data-ttu-id="4fcd3-838">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-839">Az.KeyVault</span></span>
* <span data-ttu-id="4fcd3-840">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-841">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4fcd3-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4fcd3-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4fcd3-842">Az.MachineLearning</span></span>
* <span data-ttu-id="4fcd3-843">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4fcd3-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4fcd3-844">Az.Media</span></span>
* <span data-ttu-id="4fcd3-845">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-846">Az.Monitor</span></span>
  * <span data-ttu-id="4fcd3-847">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4fcd3-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4fcd3-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4fcd3-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4fcd3-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4fcd3-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4fcd3-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4fcd3-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4fcd3-853">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="4fcd3-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-854">Az.Network</span></span>
* <span data-ttu-id="4fcd3-855">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-856">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4fcd3-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4fcd3-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4fcd3-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="4fcd3-858">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-860">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4fcd3-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4fcd3-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4fcd3-862">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-864">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-865">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4fcd3-866">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4fcd3-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4fcd3-867">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="4fcd3-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4fcd3-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4fcd3-868">Az.RedisCache</span></span>
* <span data-ttu-id="4fcd3-869">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-870">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-871">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4fcd3-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-872">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-873">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="4fcd3-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4fcd3-874">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-875">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4fcd3-876">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4fcd3-877">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4fcd3-878">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4fcd3-879">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4fcd3-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-880">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-881">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="4fcd3-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4fcd3-882">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4fcd3-883">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4fcd3-884">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4fcd3-885">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4fcd3-886">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4fcd3-886">Highlights since the last major release</span></span>
* <span data-ttu-id="4fcd3-887">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-887">General availability of `Az` module</span></span>
* <span data-ttu-id="4fcd3-888">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4fcd3-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4fcd3-889">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4fcd3-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4fcd3-890">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4fcd3-891">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4fcd3-892">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4fcd3-893">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4fcd3-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-894">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-895">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4fcd3-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4fcd3-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="4fcd3-897">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="4fcd3-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4fcd3-898">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="4fcd3-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-899">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-900">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4fcd3-901">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4fcd3-902">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-903">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-904">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4fcd3-905">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="4fcd3-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="4fcd3-907">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="4fcd3-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-908">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-909">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4fcd3-910">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-911">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-912">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="4fcd3-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4fcd3-913">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4fcd3-914">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="4fcd3-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4fcd3-915">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4fcd3-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4fcd3-916">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="4fcd3-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4fcd3-917">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4fcd3-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-918">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-919">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-920">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-921">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4fcd3-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fcd3-922">New-AzStorageContext</span></span>
* <span data-ttu-id="4fcd3-923">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4fcd3-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4fcd3-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4fcd3-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4fcd3-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4fcd3-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4fcd3-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4fcd3-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4fcd3-928">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4fcd3-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4fcd3-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4fcd3-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4fcd3-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4fcd3-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4fcd3-933">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4fcd3-934">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4fcd3-934">Highlights since the last major release</span></span>
* <span data-ttu-id="4fcd3-935">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-935">General availability of `Az` module</span></span>
* <span data-ttu-id="4fcd3-936">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4fcd3-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4fcd3-937">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4fcd3-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4fcd3-938">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4fcd3-939">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4fcd3-940">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4fcd3-941">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4fcd3-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-942">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-943">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4fcd3-944">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="4fcd3-944">Dynamic grouping</span></span>
    * <span data-ttu-id="4fcd3-945">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-945">Pre-Post script</span></span>
    * <span data-ttu-id="4fcd3-946">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="4fcd3-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-947">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-948">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4fcd3-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4fcd3-949">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-950">Az.KeyVault</span></span>
* <span data-ttu-id="4fcd3-951">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-952">Az.Network</span></span>
* <span data-ttu-id="4fcd3-953">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4fcd3-954">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-956">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4fcd3-957">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="4fcd3-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-958">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-959">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4fcd3-960">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-961">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-962">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-963">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-964">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4fcd3-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4fcd3-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4fcd3-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4fcd3-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4fcd3-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4fcd3-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4fcd3-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4fcd3-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4fcd3-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-971">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-972">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="4fcd3-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="4fcd3-973">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-974">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-975">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="4fcd3-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4fcd3-976">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-977">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-978">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4fcd3-979">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4fcd3-980">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="4fcd3-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4fcd3-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4fcd3-981">Az.Cdn</span></span>
* <span data-ttu-id="4fcd3-982">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-983">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-984">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="4fcd3-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-985">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-986">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4fcd3-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-987">Az.LogicApp</span></span>
* <span data-ttu-id="4fcd3-988">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-989">Az.Network</span></span>
* <span data-ttu-id="4fcd3-990">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-992">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4fcd3-993">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="4fcd3-993">SDK Update</span></span>
* <span data-ttu-id="4fcd3-994">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4fcd3-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4fcd3-995">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4fcd3-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-996">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-997">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4fcd3-998">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4fcd3-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4fcd3-999">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4fcd3-1000">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4fcd3-1001">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4fcd3-1002">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1003">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1004">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4fcd3-1005">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1006">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-1007">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4fcd3-1008">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4fcd3-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="4fcd3-1010">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1011">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-1012">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4fcd3-1013">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4fcd3-1014">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-1016">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1017">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1018">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4fcd3-1019">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4fcd3-1020">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4fcd3-1021">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-1023">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4fcd3-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1024">Az.EventHub</span></span>
* <span data-ttu-id="4fcd3-1025">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1026">Az.KeyVault</span></span>
* <span data-ttu-id="4fcd3-1027">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4fcd3-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1028">Az.LogicApp</span></span>
* <span data-ttu-id="4fcd3-1029">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4fcd3-1030">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4fcd3-1031">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4fcd3-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4fcd3-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4fcd3-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4fcd3-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4fcd3-1036">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4fcd3-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4fcd3-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4fcd3-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4fcd3-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4fcd3-1041">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4fcd3-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1042">Az.Monitor</span></span>
* <span data-ttu-id="4fcd3-1043">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1044">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1045">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="4fcd3-1047">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4fcd3-1048">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="4fcd3-1049">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1050">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1051">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4fcd3-1052">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4fcd3-1053">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4fcd3-1054">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1055">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1056">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4fcd3-1057">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1058">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-1059">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4fcd3-1060">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1061">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-1062">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4fcd3-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="4fcd3-1064">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1065">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1066">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4fcd3-1067">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4fcd3-1068">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="4fcd3-1070">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1071">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1072">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="4fcd3-1073">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4fcd3-1074">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="4fcd3-1075">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1076">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1077">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4fcd3-1078">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4fcd3-1079">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4fcd3-1080">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1081">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-1082">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4fcd3-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="4fcd3-1084">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="4fcd3-1086">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4fcd3-1087">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1088">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-1089">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4fcd3-1090">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4fcd3-1091">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4fcd3-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1092">Az.Aks</span></span>
* <span data-ttu-id="4fcd3-1093">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4fcd3-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1094">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-1095">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4fcd3-1096">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4fcd3-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1097">Az.Cdn</span></span>
* <span data-ttu-id="4fcd3-1098">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1099">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1100">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4fcd3-1101">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4fcd3-1102">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4fcd3-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4fcd3-1104">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4fcd3-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1105">Az.DataFactory</span></span>
* <span data-ttu-id="4fcd3-1106">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-1108">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4fcd3-1109">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4fcd3-1110">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4fcd3-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1111">Az.IotHub</span></span>
* <span data-ttu-id="4fcd3-1112">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1113">Az.KeyVault</span></span>
* <span data-ttu-id="4fcd3-1114">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1115">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1116">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1117">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1118">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4fcd3-1119">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4fcd3-1120">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4fcd3-1121">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4fcd3-1122">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4fcd3-1123">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4fcd3-1124">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-1126">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4fcd3-1127">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1127">Fix some error messages.</span></span>
* <span data-ttu-id="4fcd3-1128">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4fcd3-1129">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4fcd3-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1130">Az.SignalR</span></span>
* <span data-ttu-id="4fcd3-1131">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1132">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1133">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4fcd3-1134">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4fcd3-1135">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4fcd3-1136">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1137">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-1138">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4fcd3-1139">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4fcd3-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4fcd3-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4fcd3-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="4fcd3-1143">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1144">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-1145">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4fcd3-1146">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4fcd3-1147">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4fcd3-1148">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4fcd3-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1149">Az.Accounts</span></span>
* <span data-ttu-id="4fcd3-1150">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1151">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1152">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4fcd3-1153">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4fcd3-1154">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-1156">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4fcd3-1157">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4fcd3-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1158">Az.EventGrid</span></span>
* <span data-ttu-id="4fcd3-1159">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4fcd3-1160">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4fcd3-1161">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4fcd3-1162">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4fcd3-1163">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4fcd3-1164">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4fcd3-1165">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4fcd3-1166">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4fcd3-1167">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4fcd3-1168">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="4fcd3-1169">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4fcd3-1170">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4fcd3-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1171">Az.IotHub</span></span>
* <span data-ttu-id="4fcd3-1172">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4fcd3-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1173">Az.LogicApp</span></span>
* <span data-ttu-id="4fcd3-1174">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1175">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1176">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4fcd3-1177">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4fcd3-1178">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4fcd3-1179">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4fcd3-1180">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4fcd3-1181">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4fcd3-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1182">Az.SignalR</span></span>
* <span data-ttu-id="4fcd3-1183">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1184">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1185">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4fcd3-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1186">Az.Storage</span></span>
* <span data-ttu-id="4fcd3-1187">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4fcd3-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="4fcd3-1189">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4fcd3-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1191">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-1192">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4fcd3-1193">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4fcd3-1194">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4fcd3-1195">Geral</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1195">General</span></span>

- <span data-ttu-id="4fcd3-1196">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="4fcd3-1197">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1197">Online help for each module</span></span>
- <span data-ttu-id="4fcd3-1198">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4fcd3-1199">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4fcd3-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1200">Az.Accounts</span></span>
- <span data-ttu-id="4fcd3-1201">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="4fcd3-1202">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="4fcd3-1204">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1204">Fixes for #7002</span></span>
- <span data-ttu-id="4fcd3-1205">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4fcd3-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1206">Az.Batch</span></span>
- <span data-ttu-id="4fcd3-1207">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4fcd3-1208">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4fcd3-1209">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4fcd3-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1210">Az.Billing</span></span>
- <span data-ttu-id="4fcd3-1211">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4fcd3-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="4fcd3-1213">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4fcd3-1214">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4fcd3-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="4fcd3-1216">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4fcd3-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4fcd3-1218">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="4fcd3-1220">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4fcd3-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1221">Az.Monitor</span></span>
- <span data-ttu-id="4fcd3-1222">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4fcd3-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1223">Az.KeyVault</span></span>
- <span data-ttu-id="4fcd3-1224">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4fcd3-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="4fcd3-1226">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4fcd3-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1227">Az.Media</span></span>
- <span data-ttu-id="4fcd3-1228">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1229">Az.Network</span></span>
<span data-ttu-id="4fcd3-1230">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4fcd3-1231">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="4fcd3-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4fcd3-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4fcd3-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4fcd3-1240">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4fcd3-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4fcd3-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4fcd3-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4fcd3-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4fcd3-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4fcd3-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4fcd3-1247">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4fcd3-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4fcd3-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4fcd3-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4fcd3-1251">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4fcd3-1252">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4fcd3-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="4fcd3-1254">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4fcd3-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1255">Az.Profile</span></span>
- <span data-ttu-id="4fcd3-1256">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="4fcd3-1258">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4fcd3-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1259">Az.Resources</span></span>
- <span data-ttu-id="4fcd3-1260">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="4fcd3-1262">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4fcd3-1263">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4fcd3-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="4fcd3-1265">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4fcd3-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1266">Az.Sql</span></span>
- <span data-ttu-id="4fcd3-1267">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4fcd3-1268">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4fcd3-1269">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4fcd3-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1270">Az.Storage</span></span>
- <span data-ttu-id="4fcd3-1271">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1272">Az.Websites</span></span>
- <span data-ttu-id="4fcd3-1273">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4fcd3-1274">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4fcd3-1275">Geral</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1275">General</span></span>

* <span data-ttu-id="4fcd3-1276">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4fcd3-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1277">Az.Compute</span></span>

* <span data-ttu-id="4fcd3-1278">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="4fcd3-1280">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4fcd3-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="4fcd3-1282">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="4fcd3-1283">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4fcd3-1284">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4fcd3-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="4fcd3-1286">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4fcd3-1287">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4fcd3-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1288">Az.Resources</span></span>

* <span data-ttu-id="4fcd3-1289">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4fcd3-1290">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4fcd3-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1291">Az.Sql</span></span>

* <span data-ttu-id="4fcd3-1292">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4fcd3-1293">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4fcd3-1294">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4fcd3-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1295">Az.Storage</span></span>

* <span data-ttu-id="4fcd3-1296">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4fcd3-1297">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4fcd3-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4fcd3-1299">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="4fcd3-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4fcd3-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1302">Az.Websites</span></span>

* <span data-ttu-id="4fcd3-1303">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="4fcd3-1304">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4fcd3-1305">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4fcd3-1306">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4fcd3-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="4fcd3-1308">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4fcd3-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1309">Az.Automation</span></span>
* <span data-ttu-id="4fcd3-1310">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4fcd3-1311">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4fcd3-1312">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4fcd3-1313">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4fcd3-1314">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4fcd3-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1315">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1316">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4fcd3-1317">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4fcd3-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="4fcd3-1319">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4fcd3-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4fcd3-1321">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1322">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1323">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4fcd3-1324">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4fcd3-1325">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="4fcd3-1326">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4fcd3-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4fcd3-1328">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4fcd3-1329">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4fcd3-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4fcd3-1331">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4fcd3-1332">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4fcd3-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1333">Az.Relay</span></span>
* <span data-ttu-id="4fcd3-1334">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4fcd3-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1335">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1336">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4fcd3-1337">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4fcd3-1338">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-1340">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4fcd3-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1341">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1342">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4fcd3-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4fcd3-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4fcd3-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4fcd3-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4fcd3-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4fcd3-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4fcd3-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4fcd3-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4fcd3-1351">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4fcd3-1352">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4fcd3-1353">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4fcd3-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4fcd3-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4fcd3-1356">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4fcd3-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4fcd3-1358">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4fcd3-1359">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4fcd3-1360">Geral</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1360">General</span></span>
* <span data-ttu-id="4fcd3-1361">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4fcd3-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1362">Az.Profile</span></span>
* <span data-ttu-id="4fcd3-1363">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4fcd3-1364">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4fcd3-1365">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4fcd3-1366">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4fcd3-1367">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4fcd3-1368">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4fcd3-1369">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-1371">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1372">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1373">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4fcd3-1374">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4fcd3-1375">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-1377">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4fcd3-1378">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4fcd3-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1379">Az.Insights</span></span>
* <span data-ttu-id="4fcd3-1380">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4fcd3-1381">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4fcd3-1382">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4fcd3-1383">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1384">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1385">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4fcd3-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4fcd3-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4fcd3-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4fcd3-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4fcd3-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4fcd3-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4fcd3-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="4fcd3-1393">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1394">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1395">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4fcd3-1396">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4fcd3-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="4fcd3-1398">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4fcd3-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="4fcd3-1400">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4fcd3-1401">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4fcd3-1402">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4fcd3-1403">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4fcd3-1404">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4fcd3-1405">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4fcd3-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1406">Az.Profile</span></span>
* <span data-ttu-id="4fcd3-1407">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4fcd3-1408">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1409">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1410">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4fcd3-1411">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4fcd3-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="4fcd3-1413">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4fcd3-1414">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4fcd3-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4fcd3-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4fcd3-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1418">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1419">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4fcd3-1420">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1421">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1422">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4fcd3-1423">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4fcd3-1424">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4fcd3-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1425">Azure.Storage</span></span>
* <span data-ttu-id="4fcd3-1426">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4fcd3-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4fcd3-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4fcd3-1429">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4fcd3-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="4fcd3-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="4fcd3-1432">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4fcd3-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1433">Az.Compute</span></span>
* <span data-ttu-id="4fcd3-1434">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4fcd3-1435">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4fcd3-1436">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4fcd3-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4fcd3-1438">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4fcd3-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1439">Az.Network</span></span>
* <span data-ttu-id="4fcd3-1440">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4fcd3-1441">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1441">new cmdlets added</span></span>
    - <span data-ttu-id="4fcd3-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4fcd3-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4fcd3-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4fcd3-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4fcd3-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4fcd3-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4fcd3-1448">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4fcd3-1449">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4fcd3-1450">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4fcd3-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1451">Az.RedisCache</span></span>
* <span data-ttu-id="4fcd3-1452">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4fcd3-1453">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4fcd3-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1454">Az.Resources</span></span>
* <span data-ttu-id="4fcd3-1455">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4fcd3-1456">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4fcd3-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1457">Az.Sql</span></span>
* <span data-ttu-id="4fcd3-1458">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4fcd3-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1459">Az.Websites</span></span>
* <span data-ttu-id="4fcd3-1460">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4fcd3-1461">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4fcd3-1462">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4fcd3-1463">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="4fcd3-1463">Initial Release</span></span>