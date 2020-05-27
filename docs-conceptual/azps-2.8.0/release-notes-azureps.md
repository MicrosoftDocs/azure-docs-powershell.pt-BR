---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 0fc897579e8caef999c337303428fd12740c3606
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386095"
---
## <a name="280---october-2019"></a><span data-ttu-id="5c13d-103">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="5c13d-104">Geral</span><span class="sxs-lookup"><span data-stu-id="5c13d-104">General</span></span>
* <span data-ttu-id="5c13d-105">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c13d-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-106">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-107">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c13d-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c13d-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-108">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-109">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="5c13d-110">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="5c13d-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-111">Az.Automation</span></span>
* <span data-ttu-id="5c13d-112">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="5c13d-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="5c13d-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c13d-113">Az.Batch</span></span>
* <span data-ttu-id="5c13d-114">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c13d-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-115">Az.Compute</span></span>
* <span data-ttu-id="5c13d-116">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c13d-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5c13d-117">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="5c13d-118">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="5c13d-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="5c13d-119">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="5c13d-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-120">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-121">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="5c13d-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="5c13d-122">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="5c13d-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="5c13d-123">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-125">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="5c13d-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c13d-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c13d-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c13d-127">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="5c13d-128">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="5c13d-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="5c13d-129">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="5c13d-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="5c13d-130">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-131">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-132">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="5c13d-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="5c13d-133">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c13d-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-134">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-135">Novos receptores do grupo de ações adicionados ao New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5c13d-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="5c13d-136">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="5c13d-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="5c13d-137">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="5c13d-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="5c13d-138">Agora os Webhooks oferecem suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5c13d-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-139">Az.Network</span></span>
* <span data-ttu-id="5c13d-140">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="5c13d-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="5c13d-141">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c13d-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="5c13d-142">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c13d-142">New cmdlets added:</span></span>
        - <span data-ttu-id="5c13d-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="5c13d-144">Cmdlets atualizados com o parâmetro opcional -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="5c13d-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="5c13d-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="5c13d-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5c13d-147">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="5c13d-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="5c13d-148">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="5c13d-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="5c13d-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c13d-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c13d-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5c13d-152">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="5c13d-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="5c13d-153">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="5c13d-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="5c13d-154">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="5c13d-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="5c13d-155">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="5c13d-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c13d-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c13d-156">Az.RedisCache</span></span>
* <span data-ttu-id="5c13d-157">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="5c13d-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-158">Az.Sql</span></span>
* <span data-ttu-id="5c13d-159">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="5c13d-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-160">Az.Storage</span></span>
* <span data-ttu-id="5c13d-161">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="5c13d-162">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="5c13d-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5c13d-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c13d-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="5c13d-164">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="5c13d-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5c13d-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c13d-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c13d-166">Az.StorageSync</span></span>
* <span data-ttu-id="5c13d-167">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="5c13d-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-168">Az.Websites</span></span>
* <span data-ttu-id="5c13d-169">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="5c13d-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="5c13d-170">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5c13d-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-171">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-172">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c13d-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5c13d-173">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="5c13d-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5c13d-174">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-175">Az.Automation</span></span>
* <span data-ttu-id="5c13d-176">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="5c13d-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5c13d-177">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="5c13d-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5c13d-178">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="5c13d-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-179">Az.Compute</span></span>
* <span data-ttu-id="5c13d-180">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5c13d-181">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c13d-182">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="5c13d-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5c13d-183">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5c13d-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5c13d-184">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5c13d-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5c13d-185">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c13d-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5c13d-186">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="5c13d-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5c13d-187">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="5c13d-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5c13d-188">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5c13d-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-189">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-190">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5c13d-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5c13d-191">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="5c13d-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c13d-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c13d-192">Az.HDInsight</span></span>
* <span data-ttu-id="5c13d-193">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="5c13d-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-194">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-195">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="5c13d-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5c13d-196">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="5c13d-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5c13d-197">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c13d-197">New cmdlets are:</span></span>
    - <span data-ttu-id="5c13d-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c13d-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c13d-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c13d-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c13d-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c13d-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c13d-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c13d-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-202">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-203">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5c13d-204">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="5c13d-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5c13d-205">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="5c13d-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5c13d-206">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5c13d-207">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="5c13d-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5c13d-208">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="5c13d-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5c13d-209">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c13d-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5c13d-210">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="5c13d-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5c13d-211">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="5c13d-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5c13d-212">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="5c13d-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5c13d-213">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="5c13d-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5c13d-214">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="5c13d-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5c13d-215">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="5c13d-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5c13d-216">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c13d-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5c13d-217">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c13d-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5c13d-218">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="5c13d-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5c13d-219">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="5c13d-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5c13d-220">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5c13d-221">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="5c13d-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5c13d-222">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-222">Overall improved help files</span></span>
* <span data-ttu-id="5c13d-223">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="5c13d-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-224">Az.Network</span></span>
* <span data-ttu-id="5c13d-225">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="5c13d-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="5c13d-226">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="5c13d-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5c13d-227">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="5c13d-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5c13d-228">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="5c13d-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5c13d-229">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="5c13d-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5c13d-230">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="5c13d-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5c13d-231">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="5c13d-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5c13d-232">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5c13d-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5c13d-233">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5c13d-234">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="5c13d-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5c13d-235">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5c13d-236">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="5c13d-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5c13d-237">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-237">New cmdlets</span></span>
        - <span data-ttu-id="5c13d-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5c13d-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5c13d-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5c13d-240">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c13d-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c13d-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5c13d-241">New-VpnSite</span></span>
        - <span data-ttu-id="5c13d-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5c13d-242">Update-VpnSite</span></span>
        - <span data-ttu-id="5c13d-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-243">New-VpnConnection</span></span>
        - <span data-ttu-id="5c13d-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-244">Update-VpnConnection</span></span>
* <span data-ttu-id="5c13d-245">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="5c13d-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-247">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="5c13d-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5c13d-248">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="5c13d-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-249">Az.Resources</span></span>
* <span data-ttu-id="5c13d-250">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="5c13d-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-252">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="5c13d-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5c13d-253">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="5c13d-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5c13d-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c13d-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c13d-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c13d-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c13d-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c13d-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c13d-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5c13d-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5c13d-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c13d-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c13d-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c13d-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c13d-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c13d-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c13d-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c13d-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c13d-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5c13d-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5c13d-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c13d-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c13d-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c13d-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c13d-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c13d-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c13d-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5c13d-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5c13d-267">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5c13d-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c13d-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c13d-268">Az.SignalR</span></span>
* <span data-ttu-id="5c13d-269">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="5c13d-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-270">Az.Sql</span></span>
* <span data-ttu-id="5c13d-271">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="5c13d-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5c13d-272">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="5c13d-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5c13d-273">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5c13d-274">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c13d-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5c13d-275">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="5c13d-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-276">Az.Storage</span></span>
* <span data-ttu-id="5c13d-277">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c13d-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5c13d-278">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="5c13d-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5c13d-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5c13d-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5c13d-281">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="5c13d-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5c13d-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5c13d-283">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c13d-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5c13d-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c13d-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c13d-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c13d-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c13d-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c13d-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c13d-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c13d-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-288">Az.Websites</span></span>
* <span data-ttu-id="5c13d-289">Corrigindo o problema em que as marcas webapp eram excluídas ao migrar o aplicativo para o novo ASP</span><span class="sxs-lookup"><span data-stu-id="5c13d-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5c13d-290">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="5c13d-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5c13d-291">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="5c13d-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5c13d-292">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5c13d-293">Geral</span><span class="sxs-lookup"><span data-stu-id="5c13d-293">General</span></span>
* <span data-ttu-id="5c13d-294">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="5c13d-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c13d-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-295">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-296">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="5c13d-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c13d-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c13d-297">Az.Aks</span></span>
* <span data-ttu-id="5c13d-298">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="5c13d-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5c13d-299">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="5c13d-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c13d-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-300">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-301">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="5c13d-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5c13d-302">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="5c13d-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5c13d-303">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="5c13d-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5c13d-304">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="5c13d-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5c13d-305">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5c13d-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c13d-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c13d-306">Az.Batch</span></span>
* <span data-ttu-id="5c13d-307">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="5c13d-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c13d-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c13d-308">Az.Cdn</span></span>
* <span data-ttu-id="5c13d-309">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="5c13d-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-310">Az.Compute</span></span>
* <span data-ttu-id="5c13d-311">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5c13d-312">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c13d-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5c13d-313">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="5c13d-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5c13d-314">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5c13d-315">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5c13d-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5c13d-316">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c13d-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5c13d-317">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="5c13d-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5c13d-318">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="5c13d-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-319">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-320">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="5c13d-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5c13d-321">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="5c13d-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5c13d-322">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="5c13d-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5c13d-323">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="5c13d-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-325">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="5c13d-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c13d-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-326">Az.EventHub</span></span>
* <span data-ttu-id="5c13d-327">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5c13d-328">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="5c13d-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5c13d-329">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5c13d-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5c13d-330">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="5c13d-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5c13d-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5c13d-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5c13d-332">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c13d-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-333">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-334">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-335">Az.Network</span></span>
* <span data-ttu-id="5c13d-336">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5c13d-337">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="5c13d-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5c13d-338">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="5c13d-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5c13d-339">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="5c13d-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5c13d-340">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5c13d-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="5c13d-341">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c13d-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5c13d-342">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5c13d-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-344">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="5c13d-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5c13d-345">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="5c13d-345">Added example</span></span>
    - <span data-ttu-id="5c13d-346">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="5c13d-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5c13d-347">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5c13d-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5c13d-348">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5c13d-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-350">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-351">Az.Resources</span></span>
* <span data-ttu-id="5c13d-352">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="5c13d-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5c13d-353">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="5c13d-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5c13d-354">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="5c13d-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5c13d-355">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-356">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-357">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5c13d-358">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="5c13d-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5c13d-359">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="5c13d-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-361">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="5c13d-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5c13d-362">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5c13d-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5c13d-363">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5c13d-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5c13d-364">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="5c13d-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5c13d-365">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5c13d-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5c13d-366">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c13d-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-367">Az.Sql</span></span>
* <span data-ttu-id="5c13d-368">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="5c13d-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-369">Az.Storage</span></span>
* <span data-ttu-id="5c13d-370">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c13d-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5c13d-371">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="5c13d-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5c13d-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5c13d-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c13d-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5c13d-374">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="5c13d-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5c13d-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c13d-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-376">Az.Websites</span></span>
* <span data-ttu-id="5c13d-377">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c13d-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5c13d-378">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-379">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-380">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c13d-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5c13d-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5c13d-382">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="5c13d-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="5c13d-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-383">Az.Automation</span></span>
* <span data-ttu-id="5c13d-384">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="5c13d-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-386">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c13d-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-387">Az.Compute</span></span>
* <span data-ttu-id="5c13d-388">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="5c13d-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c13d-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c13d-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c13d-390">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="5c13d-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5c13d-391">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="5c13d-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-392">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-393">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="5c13d-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5c13d-394">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="5c13d-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c13d-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-395">Az.EventHub</span></span>
* <span data-ttu-id="5c13d-396">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5c13d-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5c13d-397">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="5c13d-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c13d-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-398">Az.KeyVault</span></span>
* <span data-ttu-id="5c13d-399">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="5c13d-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c13d-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-400">Az.LogicApp</span></span>
* <span data-ttu-id="5c13d-401">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="5c13d-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5c13d-402">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="5c13d-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5c13d-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-403">Az.ManagedServices</span></span>
* <span data-ttu-id="5c13d-404">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="5c13d-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-405">Az.Network</span></span>
* <span data-ttu-id="5c13d-406">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="5c13d-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5c13d-407">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-407">New cmdlets</span></span>
        - <span data-ttu-id="5c13d-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c13d-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c13d-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c13d-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c13d-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c13d-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c13d-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c13d-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5c13d-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5c13d-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5c13d-416">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="5c13d-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5c13d-417">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="5c13d-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5c13d-418">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c13d-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5c13d-419">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c13d-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5c13d-420">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="5c13d-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5c13d-421">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="5c13d-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5c13d-422">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="5c13d-422">Updated cmdlets</span></span>
        - <span data-ttu-id="5c13d-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c13d-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c13d-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5c13d-426">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5c13d-427">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5c13d-428">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c13d-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c13d-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5c13d-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5c13d-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5c13d-432">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="5c13d-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5c13d-433">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="5c13d-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5c13d-434">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="5c13d-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-436">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="5c13d-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="5c13d-437">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="5c13d-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-439">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5c13d-440">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5c13d-441">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5c13d-442">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5c13d-443">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5c13d-444">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5c13d-445">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5c13d-446">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5c13d-447">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5c13d-448">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="5c13d-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-449">Az.Resources</span></span>
- <span data-ttu-id="5c13d-450">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c13d-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5c13d-451">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5c13d-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-452">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-453">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5c13d-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5c13d-454">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="5c13d-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-455">Az.Sql</span></span>
* <span data-ttu-id="5c13d-456">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c13d-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5c13d-457">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="5c13d-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5c13d-458">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="5c13d-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-459">Az.Storage</span></span>
* <span data-ttu-id="5c13d-460">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="5c13d-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c13d-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c13d-461">Az.StorageSync</span></span>
* <span data-ttu-id="5c13d-462">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="5c13d-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5c13d-463">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="5c13d-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-464">Az.Websites</span></span>
* <span data-ttu-id="5c13d-465">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5c13d-466">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5c13d-467">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="5c13d-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5c13d-468">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-469">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-470">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="5c13d-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5c13d-471">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="5c13d-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5c13d-472">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c13d-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5c13d-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5c13d-473">Az.Advisor</span></span>
* <span data-ttu-id="5c13d-474">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5c13d-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5c13d-475">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="5c13d-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c13d-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-476">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-477">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="5c13d-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5c13d-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c13d-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5c13d-479">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="5c13d-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5c13d-480">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="5c13d-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5c13d-481">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="5c13d-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5c13d-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c13d-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5c13d-483">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="5c13d-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-484">Az.Automation</span></span>
* <span data-ttu-id="5c13d-485">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c13d-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-486">Az.Compute</span></span>
* <span data-ttu-id="5c13d-487">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-488">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-489">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="5c13d-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c13d-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c13d-490">Az.EventGrid</span></span>
* <span data-ttu-id="5c13d-491">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="5c13d-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-492">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-493">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="5c13d-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-494">Az.Network</span></span>
* <span data-ttu-id="5c13d-495">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="5c13d-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5c13d-496">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="5c13d-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c13d-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c13d-498">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="5c13d-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5c13d-499">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="5c13d-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-501">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5c13d-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-503">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="5c13d-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-504">Az.Resources</span></span>
    - <span data-ttu-id="5c13d-505">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="5c13d-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5c13d-506">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="5c13d-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5c13d-507">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="5c13d-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5c13d-508">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="5c13d-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-509">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-510">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="5c13d-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-511">Az.Sql</span></span>
* <span data-ttu-id="5c13d-512">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="5c13d-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5c13d-513">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c13d-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5c13d-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c13d-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c13d-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c13d-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5c13d-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5c13d-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c13d-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5c13d-520">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="5c13d-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-521">Az.Storage</span></span>
* <span data-ttu-id="5c13d-522">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c13d-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5c13d-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c13d-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5c13d-524">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="5c13d-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5c13d-525">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="5c13d-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5c13d-526">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5c13d-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5c13d-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5c13d-529">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="5c13d-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5c13d-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c13d-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5c13d-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c13d-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c13d-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c13d-532">Az.StorageSync</span></span>
* <span data-ttu-id="5c13d-533">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="5c13d-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5c13d-534">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-535">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-536">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="5c13d-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5c13d-537">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="5c13d-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5c13d-538">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="5c13d-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5c13d-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5c13d-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5c13d-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5c13d-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-541">Az.Compute</span></span>
* <span data-ttu-id="5c13d-542">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5c13d-543">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="5c13d-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5c13d-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5c13d-544">Az.Dns</span></span>
* <span data-ttu-id="5c13d-545">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c13d-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c13d-546">Az.EventGrid</span></span>
* <span data-ttu-id="5c13d-547">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="5c13d-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5c13d-548">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c13d-548">New cmdlets:</span></span>
    - <span data-ttu-id="5c13d-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c13d-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c13d-550">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c13d-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c13d-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c13d-552">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5c13d-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c13d-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c13d-554">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c13d-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5c13d-556">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c13d-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5c13d-558">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5c13d-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5c13d-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5c13d-560">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5c13d-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5c13d-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5c13d-562">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="5c13d-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="5c13d-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5c13d-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5c13d-564">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5c13d-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5c13d-565">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="5c13d-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="5c13d-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5c13d-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5c13d-567">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5c13d-568">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5c13d-569">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="5c13d-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5c13d-570">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c13d-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5c13d-571">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="5c13d-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5c13d-572">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5c13d-573">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="5c13d-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5c13d-574">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="5c13d-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="5c13d-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5c13d-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5c13d-576">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="5c13d-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5c13d-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5c13d-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5c13d-578">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5c13d-579">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c13d-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c13d-580">Az.FrontDoor</span></span>
* <span data-ttu-id="5c13d-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5c13d-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5c13d-582">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="5c13d-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5c13d-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c13d-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5c13d-584">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="5c13d-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-585">Az.Network</span></span>
* <span data-ttu-id="5c13d-586">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5c13d-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5c13d-587">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-587">New cmdlets</span></span>
        - <span data-ttu-id="5c13d-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5c13d-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5c13d-589">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5c13d-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5c13d-590">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-590">New cmdlets</span></span> 
        - <span data-ttu-id="5c13d-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5c13d-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5c13d-592">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5c13d-593">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-593">New cmdlets</span></span> 
        - <span data-ttu-id="5c13d-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="5c13d-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c13d-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c13d-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c13d-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5c13d-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5c13d-599">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c13d-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5c13d-600">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-600">New cmdlets</span></span>
        - <span data-ttu-id="5c13d-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c13d-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c13d-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c13d-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c13d-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c13d-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c13d-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5c13d-605">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c13d-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5c13d-606">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="5c13d-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5c13d-607">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="5c13d-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5c13d-608">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5c13d-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5c13d-609">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5c13d-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5c13d-610">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c13d-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5c13d-611">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5c13d-612">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="5c13d-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5c13d-613">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5c13d-614">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="5c13d-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5c13d-615">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5c13d-616">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5c13d-617">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5c13d-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5c13d-618">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5c13d-619">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="5c13d-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5c13d-620">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="5c13d-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5c13d-621">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c13d-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5c13d-622">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="5c13d-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5c13d-623">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5c13d-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="5c13d-624">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5c13d-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="5c13d-625">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5c13d-626">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5c13d-627">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-629">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="5c13d-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-630">Az.Resources</span></span>
* <span data-ttu-id="5c13d-631">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="5c13d-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5c13d-632">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5c13d-633">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5c13d-634">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="5c13d-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-636">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="5c13d-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-637">Az.Sql</span></span>
* <span data-ttu-id="5c13d-638">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c13d-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5c13d-639">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c13d-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5c13d-640">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="5c13d-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5c13d-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c13d-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c13d-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c13d-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c13d-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5c13d-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5c13d-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5c13d-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-646">Az.Storage</span></span>
* <span data-ttu-id="5c13d-647">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c13d-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5c13d-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="5c13d-649">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="5c13d-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5c13d-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-651">Az.Websites</span></span>
* <span data-ttu-id="5c13d-652">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="5c13d-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5c13d-653">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c13d-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5c13d-654">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5c13d-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c13d-655">Az.Cdn</span></span>
* <span data-ttu-id="5c13d-656">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="5c13d-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-657">Az.Compute</span></span>
* <span data-ttu-id="5c13d-658">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5c13d-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5c13d-659">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c13d-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c13d-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-660">Az.EventHub</span></span>
* <span data-ttu-id="5c13d-661">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="5c13d-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5c13d-662">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c13d-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-663">Az.Network</span></span>
* <span data-ttu-id="5c13d-664">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="5c13d-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5c13d-665">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="5c13d-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c13d-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c13d-667">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="5c13d-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-669">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="5c13d-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-670">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-671">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c13d-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-673">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="5c13d-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5c13d-674">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-675">Az.Sql</span></span>
* <span data-ttu-id="5c13d-676">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5c13d-677">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5c13d-678">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c13d-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5c13d-679">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="5c13d-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-680">Az.Websites</span></span>
* <span data-ttu-id="5c13d-681">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="5c13d-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5c13d-682">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5c13d-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-683">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-684">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5c13d-685">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5c13d-686">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5c13d-687">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="5c13d-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5c13d-688">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5c13d-689">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5c13d-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5c13d-690">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5c13d-691">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5c13d-692">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5c13d-693">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="5c13d-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5c13d-694">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5c13d-695">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="5c13d-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5c13d-696">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="5c13d-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5c13d-697">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="5c13d-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5c13d-698">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="5c13d-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5c13d-699">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="5c13d-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5c13d-700">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="5c13d-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5c13d-701">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="5c13d-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5c13d-702">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="5c13d-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="5c13d-703">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="5c13d-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5c13d-704">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="5c13d-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5c13d-705">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="5c13d-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5c13d-706">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="5c13d-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5c13d-707">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="5c13d-708">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="5c13d-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5c13d-709">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="5c13d-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5c13d-710">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5c13d-711">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5c13d-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5c13d-712">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5c13d-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5c13d-713">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="5c13d-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5c13d-714">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="5c13d-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="5c13d-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5c13d-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5c13d-716">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="5c13d-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5c13d-717">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c13d-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5c13d-718">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="5c13d-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5c13d-719">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="5c13d-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5c13d-720">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="5c13d-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5c13d-721">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="5c13d-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5c13d-722">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="5c13d-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5c13d-723">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c13d-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="5c13d-724">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5c13d-725">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c13d-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5c13d-726">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5c13d-727">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="5c13d-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5c13d-728">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c13d-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5c13d-729">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5c13d-730">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c13d-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="5c13d-731">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="5c13d-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5c13d-732">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="5c13d-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5c13d-733">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5c13d-734">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="5c13d-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5c13d-735">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="5c13d-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5c13d-736">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="5c13d-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5c13d-737">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="5c13d-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5c13d-738">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="5c13d-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5c13d-739">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c13d-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5c13d-740">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c13d-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5c13d-741">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c13d-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5c13d-742">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c13d-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5c13d-743">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c13d-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5c13d-744">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c13d-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5c13d-745">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c13d-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5c13d-746">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c13d-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5c13d-747">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c13d-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5c13d-748">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="5c13d-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5c13d-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="5c13d-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5c13d-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5c13d-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5c13d-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="5c13d-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5c13d-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5c13d-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5c13d-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c13d-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5c13d-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5c13d-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5c13d-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5c13d-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5c13d-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="5c13d-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5c13d-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5c13d-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c13d-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="5c13d-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c13d-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5c13d-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="5c13d-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-761">Az.Automation</span></span>
* <span data-ttu-id="5c13d-762">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="5c13d-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5c13d-763">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="5c13d-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5c13d-764">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="5c13d-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5c13d-765">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="5c13d-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5c13d-766">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="5c13d-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5c13d-767">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="5c13d-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5c13d-768">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="5c13d-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-769">Az.Compute</span></span>
* <span data-ttu-id="5c13d-770">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="5c13d-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5c13d-771">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="5c13d-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-773">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-774">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-775">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-776">Az.Network</span></span>
* <span data-ttu-id="5c13d-777">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="5c13d-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5c13d-778">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c13d-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c13d-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c13d-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5c13d-780">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5c13d-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-781">Az.Resources</span></span>
* <span data-ttu-id="5c13d-782">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="5c13d-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-783">Az.Sql</span></span>
* <span data-ttu-id="5c13d-784">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="5c13d-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5c13d-785">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-786">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-787">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="5c13d-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-789">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="5c13d-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5c13d-790">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="5c13d-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-791">Az.Compute</span></span>
* <span data-ttu-id="5c13d-792">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="5c13d-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5c13d-793">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5c13d-794">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5c13d-795">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="5c13d-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5c13d-796">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="5c13d-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5c13d-797">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c13d-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="5c13d-798">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="5c13d-798">Breaking changes</span></span>
    - <span data-ttu-id="5c13d-799">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="5c13d-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5c13d-800">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="5c13d-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5c13d-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5c13d-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="5c13d-802">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5c13d-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5c13d-803">Az.Dns</span></span>
* <span data-ttu-id="5c13d-804">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="5c13d-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5c13d-805">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="5c13d-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5c13d-806">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c13d-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c13d-807">Az.FrontDoor</span></span>
* <span data-ttu-id="5c13d-808">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5c13d-809">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="5c13d-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5c13d-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c13d-810">Az.HDInsight</span></span>
* <span data-ttu-id="5c13d-811">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c13d-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5c13d-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c13d-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5c13d-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c13d-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5c13d-814">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c13d-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5c13d-815">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="5c13d-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5c13d-816">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="5c13d-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5c13d-817">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="5c13d-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-818">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-819">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="5c13d-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="5c13d-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5c13d-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5c13d-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5c13d-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5c13d-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5c13d-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5c13d-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5c13d-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5c13d-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5c13d-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5c13d-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5c13d-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c13d-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c13d-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c13d-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c13d-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c13d-831">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="5c13d-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5c13d-832">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="5c13d-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-833">Az.Network</span></span>
* <span data-ttu-id="5c13d-834">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="5c13d-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5c13d-835">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c13d-835">New cmdlets</span></span>
        - <span data-ttu-id="5c13d-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="5c13d-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5c13d-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5c13d-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5c13d-840">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="5c13d-840">Updated cmdlets</span></span>
        - <span data-ttu-id="5c13d-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5c13d-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5c13d-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5c13d-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5c13d-843">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="5c13d-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5c13d-844">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5c13d-845">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c13d-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c13d-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c13d-847">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="5c13d-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5c13d-848">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="5c13d-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5c13d-849">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-851">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c13d-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5c13d-852">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c13d-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5c13d-853">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c13d-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5c13d-854">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5c13d-855">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c13d-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5c13d-856">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="5c13d-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5c13d-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5c13d-857">Az.Relay</span></span>
* <span data-ttu-id="5c13d-858">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="5c13d-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-859">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-860">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="5c13d-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-861">Az.Storage</span></span>
* <span data-ttu-id="5c13d-862">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="5c13d-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5c13d-863">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="5c13d-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5c13d-864">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="5c13d-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5c13d-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="5c13d-866">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="5c13d-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5c13d-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5c13d-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5c13d-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-870">Az.Websites</span></span>
* <span data-ttu-id="5c13d-871">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5c13d-872">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="5c13d-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5c13d-873">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c13d-874">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c13d-874">Highlights since the last major release</span></span>
* <span data-ttu-id="5c13d-875">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c13d-875">General availability of `Az` module</span></span>
* <span data-ttu-id="5c13d-876">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c13d-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c13d-877">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c13d-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c13d-878">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c13d-879">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c13d-880">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c13d-881">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c13d-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c13d-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-882">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-883">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="5c13d-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c13d-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c13d-884">Az.Batch</span></span>
* <span data-ttu-id="5c13d-885">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c13d-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c13d-886">Az.Cdn</span></span>
* <span data-ttu-id="5c13d-887">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-889">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-890">Az.Compute</span></span>
* <span data-ttu-id="5c13d-891">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c13d-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5c13d-892">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-893">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c13d-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-894">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-895">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c13d-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-897">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c13d-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c13d-898">Az.EventGrid</span></span>
* <span data-ttu-id="5c13d-899">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="5c13d-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c13d-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-900">Az.EventHub</span></span>
* <span data-ttu-id="5c13d-901">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="5c13d-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5c13d-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c13d-902">Az.HDInsight</span></span>
* <span data-ttu-id="5c13d-903">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-904">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-905">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c13d-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-906">Az.KeyVault</span></span>
* <span data-ttu-id="5c13d-907">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-908">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c13d-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5c13d-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c13d-909">Az.MachineLearning</span></span>
* <span data-ttu-id="5c13d-910">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5c13d-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c13d-911">Az.Media</span></span>
* <span data-ttu-id="5c13d-912">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-913">Az.Monitor</span></span>
  * <span data-ttu-id="5c13d-914">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="5c13d-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5c13d-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5c13d-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5c13d-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5c13d-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5c13d-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c13d-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c13d-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c13d-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c13d-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c13d-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5c13d-920">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="5c13d-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-921">Az.Network</span></span>
* <span data-ttu-id="5c13d-922">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-923">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c13d-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5c13d-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5c13d-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="5c13d-925">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-927">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5c13d-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5c13d-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5c13d-929">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-931">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-932">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5c13d-933">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5c13d-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5c13d-934">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="5c13d-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c13d-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c13d-935">Az.RedisCache</span></span>
* <span data-ttu-id="5c13d-936">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-937">Az.Resources</span></span>
* <span data-ttu-id="5c13d-938">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c13d-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-939">Az.Sql</span></span>
* <span data-ttu-id="5c13d-940">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="5c13d-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5c13d-941">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-942">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="5c13d-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5c13d-943">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="5c13d-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5c13d-944">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="5c13d-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5c13d-945">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5c13d-946">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c13d-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-947">Az.Websites</span></span>
* <span data-ttu-id="5c13d-948">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="5c13d-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5c13d-949">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c13d-950">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="5c13d-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5c13d-951">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="5c13d-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5c13d-952">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c13d-953">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c13d-953">Highlights since the last major release</span></span>
* <span data-ttu-id="5c13d-954">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c13d-954">General availability of `Az` module</span></span>
* <span data-ttu-id="5c13d-955">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c13d-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c13d-956">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c13d-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c13d-957">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c13d-958">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c13d-959">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c13d-960">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c13d-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c13d-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-961">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-962">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="5c13d-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c13d-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c13d-964">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="5c13d-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5c13d-965">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="5c13d-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-966">Az.Automation</span></span>
* <span data-ttu-id="5c13d-967">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="5c13d-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5c13d-968">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="5c13d-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5c13d-969">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-970">Az.Compute</span></span>
* <span data-ttu-id="5c13d-971">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c13d-972">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="5c13d-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="5c13d-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c13d-974">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="5c13d-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-975">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-976">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="5c13d-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5c13d-977">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c13d-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-978">Az.Resources</span></span>
* <span data-ttu-id="5c13d-979">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="5c13d-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5c13d-980">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c13d-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5c13d-981">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="5c13d-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5c13d-982">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c13d-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5c13d-983">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="5c13d-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5c13d-984">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c13d-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-985">Az.Sql</span></span>
* <span data-ttu-id="5c13d-986">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="5c13d-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-987">Az.Storage</span></span>
* <span data-ttu-id="5c13d-988">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5c13d-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c13d-989">New-AzStorageContext</span></span>
* <span data-ttu-id="5c13d-990">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c13d-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5c13d-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c13d-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c13d-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c13d-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c13d-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5c13d-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5c13d-995">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="5c13d-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5c13d-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c13d-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c13d-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5c13d-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c13d-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5c13d-1000">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c13d-1001">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c13d-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="5c13d-1002">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c13d-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="5c13d-1003">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c13d-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c13d-1004">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c13d-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c13d-1005">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c13d-1006">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c13d-1007">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c13d-1008">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c13d-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1009">Az.Automation</span></span>
* <span data-ttu-id="5c13d-1010">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="5c13d-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5c13d-1011">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c13d-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="5c13d-1012">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="5c13d-1012">Pre-Post script</span></span>
    * <span data-ttu-id="5c13d-1013">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="5c13d-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1014">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1015">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5c13d-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5c13d-1016">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c13d-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-1017">Az.KeyVault</span></span>
* <span data-ttu-id="5c13d-1018">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1019">Az.Network</span></span>
* <span data-ttu-id="5c13d-1020">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5c13d-1021">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="5c13d-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-1023">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5c13d-1024">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="5c13d-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1025">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1026">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c13d-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5c13d-1027">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="5c13d-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1028">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1029">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1030">Az.Storage</span></span>
* <span data-ttu-id="5c13d-1031">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c13d-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5c13d-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c13d-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c13d-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c13d-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5c13d-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5c13d-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5c13d-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5c13d-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1038">Az.Websites</span></span>
* <span data-ttu-id="5c13d-1039">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="5c13d-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="5c13d-1040">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1041">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-1042">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="5c13d-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5c13d-1043">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1044">Az.Automation</span></span>
* <span data-ttu-id="5c13d-1045">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c13d-1046">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5c13d-1047">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="5c13d-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c13d-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c13d-1048">Az.Cdn</span></span>
* <span data-ttu-id="5c13d-1049">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1050">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1051">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="5c13d-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-1052">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-1053">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c13d-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-1054">Az.LogicApp</span></span>
* <span data-ttu-id="5c13d-1055">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1056">Az.Network</span></span>
* <span data-ttu-id="5c13d-1057">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-1059">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5c13d-1060">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="5c13d-1060">SDK Update</span></span>
* <span data-ttu-id="5c13d-1061">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c13d-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5c13d-1062">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c13d-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1063">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1064">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="5c13d-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5c13d-1065">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="5c13d-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5c13d-1066">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c13d-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5c13d-1067">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="5c13d-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5c13d-1068">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c13d-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5c13d-1069">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="5c13d-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1070">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1071">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5c13d-1072">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1073">Az.Storage</span></span>
* <span data-ttu-id="5c13d-1074">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5c13d-1075">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5c13d-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c13d-1077">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1078">Az.Automation</span></span>
* <span data-ttu-id="5c13d-1079">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5c13d-1080">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5c13d-1081">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-1083">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1084">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1085">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="5c13d-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5c13d-1086">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="5c13d-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5c13d-1087">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5c13d-1088">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-1090">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c13d-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-1091">Az.EventHub</span></span>
* <span data-ttu-id="5c13d-1092">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5c13d-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-1093">Az.KeyVault</span></span>
* <span data-ttu-id="5c13d-1094">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c13d-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c13d-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-1095">Az.LogicApp</span></span>
* <span data-ttu-id="5c13d-1096">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="5c13d-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5c13d-1097">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="5c13d-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5c13d-1098">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c13d-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5c13d-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c13d-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c13d-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c13d-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c13d-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c13d-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c13d-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c13d-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5c13d-1103">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c13d-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5c13d-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c13d-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c13d-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c13d-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5c13d-1108">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c13d-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-1109">Az.Monitor</span></span>
* <span data-ttu-id="5c13d-1110">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5c13d-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1111">Az.Network</span></span>
* <span data-ttu-id="5c13d-1112">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5c13d-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c13d-1114">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5c13d-1115">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5c13d-1116">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5c13d-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1117">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1118">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c13d-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c13d-1119">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c13d-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5c13d-1120">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="5c13d-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5c13d-1121">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5c13d-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1122">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1123">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5c13d-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5c13d-1124">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="5c13d-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1125">Az.Websites</span></span>
* <span data-ttu-id="5c13d-1126">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="5c13d-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5c13d-1127">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1128">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-1129">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c13d-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c13d-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="5c13d-1131">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1132">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1133">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="5c13d-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5c13d-1134">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5c13d-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5c13d-1135">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="5c13d-1137">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1138">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1139">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5c13d-1140">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c13d-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c13d-1141">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="5c13d-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5c13d-1142">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c13d-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1143">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1144">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5c13d-1145">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="5c13d-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5c13d-1146">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5c13d-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5c13d-1147">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1148">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-1149">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="5c13d-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c13d-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c13d-1151">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c13d-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c13d-1153">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c13d-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5c13d-1154">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1155">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-1156">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c13d-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c13d-1157">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c13d-1158">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5c13d-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c13d-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c13d-1159">Az.Aks</span></span>
* <span data-ttu-id="5c13d-1160">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c13d-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1161">Az.Automation</span></span>
* <span data-ttu-id="5c13d-1162">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="5c13d-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5c13d-1163">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c13d-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c13d-1164">Az.Cdn</span></span>
* <span data-ttu-id="5c13d-1165">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1166">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1167">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5c13d-1168">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c13d-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5c13d-1169">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c13d-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c13d-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c13d-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c13d-1171">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c13d-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c13d-1172">Az.DataFactory</span></span>
* <span data-ttu-id="5c13d-1173">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5c13d-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-1175">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c13d-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5c13d-1176">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5c13d-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5c13d-1177">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-1178">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-1179">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c13d-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-1180">Az.KeyVault</span></span>
* <span data-ttu-id="5c13d-1181">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1182">Az.Network</span></span>
* <span data-ttu-id="5c13d-1183">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1184">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1185">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="5c13d-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5c13d-1186">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5c13d-1187">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="5c13d-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5c13d-1188">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="5c13d-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5c13d-1189">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="5c13d-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5c13d-1190">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c13d-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5c13d-1191">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5c13d-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-1193">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5c13d-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5c13d-1194">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1194">Fix some error messages.</span></span>
* <span data-ttu-id="5c13d-1195">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5c13d-1196">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c13d-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c13d-1197">Az.SignalR</span></span>
* <span data-ttu-id="5c13d-1198">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1199">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1200">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c13d-1201">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5c13d-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5c13d-1202">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="5c13d-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5c13d-1203">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="5c13d-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1204">Az.Storage</span></span>
* <span data-ttu-id="5c13d-1205">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c13d-1206">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5c13d-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5c13d-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5c13d-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5c13d-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5c13d-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c13d-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="5c13d-1210">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1211">Az.Websites</span></span>
* <span data-ttu-id="5c13d-1212">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c13d-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c13d-1213">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5c13d-1214">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5c13d-1215">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c13d-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c13d-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1216">Az.Accounts</span></span>
* <span data-ttu-id="5c13d-1217">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5c13d-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1218">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1219">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5c13d-1220">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c13d-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5c13d-1221">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-1223">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5c13d-1224">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="5c13d-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c13d-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c13d-1225">Az.EventGrid</span></span>
* <span data-ttu-id="5c13d-1226">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5c13d-1227">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5c13d-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5c13d-1228">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c13d-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c13d-1229">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c13d-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c13d-1230">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c13d-1231">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c13d-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5c13d-1232">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c13d-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c13d-1233">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c13d-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c13d-1234">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c13d-1235">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c13d-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="5c13d-1236">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5c13d-1237">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c13d-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-1238">Az.IotHub</span></span>
* <span data-ttu-id="5c13d-1239">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="5c13d-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c13d-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c13d-1240">Az.LogicApp</span></span>
* <span data-ttu-id="5c13d-1241">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="5c13d-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1242">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1243">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="5c13d-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5c13d-1244">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5c13d-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5c13d-1245">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c13d-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c13d-1246">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5c13d-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5c13d-1247">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="5c13d-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5c13d-1248">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5c13d-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c13d-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c13d-1249">Az.SignalR</span></span>
* <span data-ttu-id="5c13d-1250">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1251">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1252">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c13d-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1253">Az.Storage</span></span>
* <span data-ttu-id="5c13d-1254">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="5c13d-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5c13d-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c13d-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="5c13d-1256">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5c13d-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5c13d-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1258">Az.Websites</span></span>
* <span data-ttu-id="5c13d-1259">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="5c13d-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5c13d-1260">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5c13d-1261">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5c13d-1262">Geral</span><span class="sxs-lookup"><span data-stu-id="5c13d-1262">General</span></span>

- <span data-ttu-id="5c13d-1263">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="5c13d-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="5c13d-1264">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1264">Online help for each module</span></span>
- <span data-ttu-id="5c13d-1265">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5c13d-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5c13d-1266">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="5c13d-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5c13d-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1267">Az.Accounts</span></span>
- <span data-ttu-id="5c13d-1268">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="5c13d-1269">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="5c13d-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c13d-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="5c13d-1271">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="5c13d-1271">Fixes for #7002</span></span>
- <span data-ttu-id="5c13d-1272">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5c13d-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c13d-1273">Az.Batch</span></span>
- <span data-ttu-id="5c13d-1274">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5c13d-1275">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5c13d-1276">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5c13d-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c13d-1277">Az.Billing</span></span>
- <span data-ttu-id="5c13d-1278">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5c13d-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="5c13d-1280">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5c13d-1281">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="5c13d-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c13d-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="5c13d-1283">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c13d-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5c13d-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c13d-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5c13d-1285">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="5c13d-1287">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5c13d-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c13d-1288">Az.Monitor</span></span>
- <span data-ttu-id="5c13d-1289">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5c13d-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c13d-1290">Az.KeyVault</span></span>
- <span data-ttu-id="5c13d-1291">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="5c13d-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5c13d-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c13d-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="5c13d-1293">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5c13d-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c13d-1294">Az.Media</span></span>
- <span data-ttu-id="5c13d-1295">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5c13d-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c13d-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1296">Az.Network</span></span>
<span data-ttu-id="5c13d-1297">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5c13d-1298">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c13d-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="5c13d-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5c13d-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5c13d-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c13d-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5c13d-1307">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5c13d-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c13d-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5c13d-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c13d-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c13d-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c13d-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5c13d-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5c13d-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5c13d-1314">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c13d-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5c13d-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c13d-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c13d-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c13d-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c13d-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c13d-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5c13d-1318">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c13d-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5c13d-1319">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5c13d-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="5c13d-1321">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5c13d-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1322">Az.Profile</span></span>
- <span data-ttu-id="5c13d-1323">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c13d-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="5c13d-1325">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5c13d-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1326">Az.Resources</span></span>
- <span data-ttu-id="5c13d-1327">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c13d-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="5c13d-1329">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="5c13d-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5c13d-1330">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5c13d-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c13d-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="5c13d-1332">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c13d-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5c13d-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1333">Az.Sql</span></span>
- <span data-ttu-id="5c13d-1334">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="5c13d-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5c13d-1335">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="5c13d-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5c13d-1336">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c13d-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1337">Az.Storage</span></span>
- <span data-ttu-id="5c13d-1338">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c13d-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1339">Az.Websites</span></span>
- <span data-ttu-id="5c13d-1340">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c13d-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5c13d-1341">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5c13d-1342">Geral</span><span class="sxs-lookup"><span data-stu-id="5c13d-1342">General</span></span>

* <span data-ttu-id="5c13d-1343">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c13d-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c13d-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1344">Az.Compute</span></span>

* <span data-ttu-id="5c13d-1345">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="5c13d-1347">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="5c13d-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5c13d-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c13d-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="5c13d-1349">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="5c13d-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="5c13d-1350">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5c13d-1351">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c13d-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="5c13d-1353">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5c13d-1354">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c13d-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1355">Az.Resources</span></span>

* <span data-ttu-id="5c13d-1356">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5c13d-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5c13d-1357">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5c13d-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1358">Az.Sql</span></span>

* <span data-ttu-id="5c13d-1359">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c13d-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5c13d-1360">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="5c13d-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5c13d-1361">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c13d-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1362">Az.Storage</span></span>

* <span data-ttu-id="5c13d-1363">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5c13d-1364">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="5c13d-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5c13d-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c13d-1366">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="5c13d-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="5c13d-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c13d-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5c13d-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c13d-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c13d-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1369">Az.Websites</span></span>

* <span data-ttu-id="5c13d-1370">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c13d-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5c13d-1371">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5c13d-1372">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5c13d-1373">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c13d-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c13d-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="5c13d-1375">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5c13d-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c13d-1376">Az.Automation</span></span>
* <span data-ttu-id="5c13d-1377">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="5c13d-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c13d-1378">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5c13d-1379">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5c13d-1380">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="5c13d-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5c13d-1381">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="5c13d-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c13d-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1382">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1383">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5c13d-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5c13d-1384">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c13d-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c13d-1386">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5c13d-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5c13d-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5c13d-1388">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="5c13d-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c13d-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1389">Az.Network</span></span>
* <span data-ttu-id="5c13d-1390">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5c13d-1391">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="5c13d-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5c13d-1392">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5c13d-1393">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5c13d-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5c13d-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c13d-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c13d-1395">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5c13d-1396">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5c13d-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5c13d-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5c13d-1398">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c13d-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5c13d-1399">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c13d-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5c13d-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5c13d-1400">Az.Relay</span></span>
* <span data-ttu-id="5c13d-1401">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c13d-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1402">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1403">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="5c13d-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5c13d-1404">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="5c13d-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5c13d-1405">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5c13d-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c13d-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-1407">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="5c13d-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5c13d-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1408">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1409">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="5c13d-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5c13d-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c13d-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c13d-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c13d-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c13d-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c13d-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c13d-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c13d-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c13d-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c13d-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c13d-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c13d-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c13d-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5c13d-1418">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5c13d-1419">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5c13d-1420">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5c13d-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c13d-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c13d-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5c13d-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5c13d-1425">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c13d-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5c13d-1426">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5c13d-1427">Geral</span><span class="sxs-lookup"><span data-stu-id="5c13d-1427">General</span></span>
* <span data-ttu-id="5c13d-1428">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="5c13d-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5c13d-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1429">Az.Profile</span></span>
* <span data-ttu-id="5c13d-1430">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c13d-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5c13d-1431">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="5c13d-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5c13d-1432">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c13d-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5c13d-1433">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="5c13d-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5c13d-1434">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="5c13d-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5c13d-1435">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c13d-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5c13d-1436">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="5c13d-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-1438">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1439">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1440">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c13d-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5c13d-1441">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5c13d-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5c13d-1442">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-1444">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5c13d-1445">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5c13d-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5c13d-1446">Az.Insights</span></span>
* <span data-ttu-id="5c13d-1447">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="5c13d-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5c13d-1448">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="5c13d-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5c13d-1449">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="5c13d-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5c13d-1450">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="5c13d-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1451">Az.Network</span></span>
* <span data-ttu-id="5c13d-1452">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="5c13d-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5c13d-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c13d-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5c13d-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5c13d-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5c13d-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c13d-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5c13d-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5c13d-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5c13d-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c13d-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5c13d-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c13d-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c13d-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c13d-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c13d-1460">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="5c13d-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1461">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1462">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5c13d-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5c13d-1463">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="5c13d-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c13d-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c13d-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="5c13d-1465">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c13d-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c13d-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c13d-1467">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5c13d-1468">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="5c13d-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5c13d-1469">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="5c13d-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5c13d-1470">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5c13d-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5c13d-1471">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5c13d-1472">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5c13d-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1473">Az.Profile</span></span>
* <span data-ttu-id="5c13d-1474">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="5c13d-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5c13d-1475">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c13d-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1476">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1477">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="5c13d-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5c13d-1478">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c13d-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c13d-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c13d-1480">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c13d-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5c13d-1481">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5c13d-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c13d-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c13d-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1485">Az.Network</span></span>
* <span data-ttu-id="5c13d-1486">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5c13d-1487">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1488">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1489">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5c13d-1490">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5c13d-1491">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5c13d-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1492">Azure.Storage</span></span>
* <span data-ttu-id="5c13d-1493">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5c13d-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5c13d-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c13d-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c13d-1496">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5c13d-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5c13d-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5c13d-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c13d-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c13d-1499">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c13d-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c13d-1500">Az.Compute</span></span>
* <span data-ttu-id="5c13d-1501">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="5c13d-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5c13d-1502">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5c13d-1503">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="5c13d-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5c13d-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5c13d-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5c13d-1505">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c13d-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c13d-1506">Az.Network</span></span>
* <span data-ttu-id="5c13d-1507">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5c13d-1508">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="5c13d-1508">new cmdlets added</span></span>
    - <span data-ttu-id="5c13d-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c13d-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c13d-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c13d-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c13d-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c13d-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5c13d-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5c13d-1515">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="5c13d-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5c13d-1516">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c13d-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5c13d-1517">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c13d-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c13d-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c13d-1518">Az.RedisCache</span></span>
* <span data-ttu-id="5c13d-1519">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="5c13d-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5c13d-1520">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="5c13d-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c13d-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c13d-1521">Az.Resources</span></span>
* <span data-ttu-id="5c13d-1522">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c13d-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c13d-1523">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="5c13d-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c13d-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c13d-1524">Az.Sql</span></span>
* <span data-ttu-id="5c13d-1525">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="5c13d-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c13d-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c13d-1526">Az.Websites</span></span>
* <span data-ttu-id="5c13d-1527">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="5c13d-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5c13d-1528">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="5c13d-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5c13d-1529">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c13d-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5c13d-1530">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="5c13d-1530">Initial Release</span></span>
