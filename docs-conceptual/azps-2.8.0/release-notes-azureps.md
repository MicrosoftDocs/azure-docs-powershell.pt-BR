---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 83e6039153bcc2b8ccb7ceddfa91609f0d6c7b3f
ms.sourcegitcommit: b4ee3fbaaa2a329ea28308bd1902ae83a34db698
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2019
ms.locfileid: "72380193"
---
## <a name="280---october-2019"></a><span data-ttu-id="ecddd-103">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ecddd-104">Geral</span><span class="sxs-lookup"><span data-stu-id="ecddd-104">General</span></span>
* <span data-ttu-id="ecddd-105">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ecddd-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-106">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-107">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="ecddd-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ecddd-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-108">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-109">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ecddd-110">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ecddd-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-111">Az.Automation</span></span>
* <span data-ttu-id="ecddd-112">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="ecddd-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="ecddd-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ecddd-113">Az.Batch</span></span>
* <span data-ttu-id="ecddd-114">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ecddd-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-115">Az.Compute</span></span>
* <span data-ttu-id="ecddd-116">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecddd-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ecddd-117">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ecddd-118">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ecddd-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="ecddd-119">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="ecddd-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-120">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-121">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ecddd-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ecddd-122">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ecddd-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ecddd-123">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-125">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="ecddd-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ecddd-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ecddd-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="ecddd-127">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ecddd-128">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ecddd-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ecddd-129">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="ecddd-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ecddd-130">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-131">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-132">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ecddd-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ecddd-133">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecddd-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-134">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-135">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ecddd-135">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ecddd-136">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="ecddd-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ecddd-137">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="ecddd-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ecddd-138">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ecddd-138">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-139">Az.Network</span></span>
* <span data-ttu-id="ecddd-140">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="ecddd-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ecddd-141">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="ecddd-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ecddd-142">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="ecddd-142">New cmdlets added:</span></span>
        - <span data-ttu-id="ecddd-143">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-143">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ecddd-144">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ecddd-145">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="ecddd-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ecddd-146">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="ecddd-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="ecddd-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ecddd-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ecddd-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ecddd-150">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="ecddd-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ecddd-151">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ecddd-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ecddd-152">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ecddd-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ecddd-153">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ecddd-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ecddd-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ecddd-154">Az.RedisCache</span></span>
* <span data-ttu-id="ecddd-155">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="ecddd-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-156">Az.Sql</span></span>
* <span data-ttu-id="ecddd-157">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="ecddd-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-158">Az.Storage</span></span>
* <span data-ttu-id="ecddd-159">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ecddd-160">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ecddd-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ecddd-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ecddd-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ecddd-162">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ecddd-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ecddd-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ecddd-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ecddd-164">Az.StorageSync</span></span>
* <span data-ttu-id="ecddd-165">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ecddd-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-166">Az.Websites</span></span>
* <span data-ttu-id="ecddd-167">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="ecddd-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ecddd-168">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ecddd-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-169">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-170">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="ecddd-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ecddd-171">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="ecddd-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ecddd-172">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-173">Az.Automation</span></span>
* <span data-ttu-id="ecddd-174">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="ecddd-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ecddd-175">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ecddd-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ecddd-176">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="ecddd-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-177">Az.Compute</span></span>
* <span data-ttu-id="ecddd-178">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ecddd-179">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ecddd-180">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="ecddd-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ecddd-181">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ecddd-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ecddd-182">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ecddd-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ecddd-183">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="ecddd-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ecddd-184">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ecddd-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ecddd-185">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="ecddd-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ecddd-186">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ecddd-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-187">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-188">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ecddd-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ecddd-189">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ecddd-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ecddd-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ecddd-190">Az.HDInsight</span></span>
* <span data-ttu-id="ecddd-191">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="ecddd-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-192">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-193">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="ecddd-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ecddd-194">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="ecddd-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ecddd-195">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="ecddd-195">New cmdlets are:</span></span>
    - <span data-ttu-id="ecddd-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ecddd-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ecddd-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ecddd-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ecddd-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ecddd-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ecddd-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ecddd-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-200">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-201">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ecddd-202">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="ecddd-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ecddd-203">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="ecddd-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ecddd-204">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="ecddd-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ecddd-205">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="ecddd-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ecddd-206">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ecddd-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ecddd-207">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ecddd-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ecddd-208">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="ecddd-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ecddd-209">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="ecddd-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ecddd-210">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="ecddd-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ecddd-211">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="ecddd-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ecddd-212">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="ecddd-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ecddd-213">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="ecddd-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ecddd-214">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="ecddd-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ecddd-215">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="ecddd-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ecddd-216">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="ecddd-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ecddd-217">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="ecddd-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ecddd-218">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ecddd-219">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="ecddd-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ecddd-220">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-220">Overall improved help files</span></span>
* <span data-ttu-id="ecddd-221">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="ecddd-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-222">Az.Network</span></span>
* <span data-ttu-id="ecddd-223">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="ecddd-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="ecddd-224">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="ecddd-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ecddd-225">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="ecddd-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ecddd-226">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="ecddd-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ecddd-227">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="ecddd-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ecddd-228">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="ecddd-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ecddd-229">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="ecddd-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ecddd-230">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ecddd-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ecddd-231">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ecddd-232">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ecddd-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ecddd-233">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ecddd-234">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="ecddd-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ecddd-235">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-235">New cmdlets</span></span>
        - <span data-ttu-id="ecddd-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ecddd-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ecddd-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ecddd-238">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ecddd-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="ecddd-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ecddd-239">New-VpnSite</span></span>
        - <span data-ttu-id="ecddd-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ecddd-240">Update-VpnSite</span></span>
        - <span data-ttu-id="ecddd-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-241">New-VpnConnection</span></span>
        - <span data-ttu-id="ecddd-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-242">Update-VpnConnection</span></span>
* <span data-ttu-id="ecddd-243">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="ecddd-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-245">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="ecddd-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ecddd-246">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="ecddd-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-247">Az.Resources</span></span>
* <span data-ttu-id="ecddd-248">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="ecddd-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-250">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ecddd-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ecddd-251">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="ecddd-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ecddd-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ecddd-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ecddd-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ecddd-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ecddd-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ecddd-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ecddd-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ecddd-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ecddd-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ecddd-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ecddd-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ecddd-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ecddd-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ecddd-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ecddd-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ecddd-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ecddd-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ecddd-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ecddd-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ecddd-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ecddd-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ecddd-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ecddd-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ecddd-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ecddd-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ecddd-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ecddd-265">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ecddd-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ecddd-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ecddd-266">Az.SignalR</span></span>
* <span data-ttu-id="ecddd-267">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="ecddd-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-268">Az.Sql</span></span>
* <span data-ttu-id="ecddd-269">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="ecddd-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ecddd-270">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="ecddd-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ecddd-271">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ecddd-272">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ecddd-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ecddd-273">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ecddd-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-274">Az.Storage</span></span>
* <span data-ttu-id="ecddd-275">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ecddd-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ecddd-276">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="ecddd-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ecddd-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ecddd-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ecddd-279">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="ecddd-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ecddd-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ecddd-281">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ecddd-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ecddd-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecddd-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ecddd-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecddd-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ecddd-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecddd-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ecddd-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecddd-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-286">Az.Websites</span></span>
* <span data-ttu-id="ecddd-287">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="ecddd-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ecddd-288">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="ecddd-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ecddd-289">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="ecddd-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ecddd-290">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ecddd-291">Geral</span><span class="sxs-lookup"><span data-stu-id="ecddd-291">General</span></span>
* <span data-ttu-id="ecddd-292">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="ecddd-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ecddd-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-293">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-294">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="ecddd-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ecddd-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ecddd-295">Az.Aks</span></span>
* <span data-ttu-id="ecddd-296">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="ecddd-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ecddd-297">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ecddd-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ecddd-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-298">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-299">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ecddd-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ecddd-300">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="ecddd-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ecddd-301">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="ecddd-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ecddd-302">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ecddd-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ecddd-303">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ecddd-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ecddd-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ecddd-304">Az.Batch</span></span>
* <span data-ttu-id="ecddd-305">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="ecddd-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ecddd-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ecddd-306">Az.Cdn</span></span>
* <span data-ttu-id="ecddd-307">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="ecddd-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-308">Az.Compute</span></span>
* <span data-ttu-id="ecddd-309">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ecddd-310">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecddd-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ecddd-311">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="ecddd-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ecddd-312">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ecddd-313">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ecddd-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ecddd-314">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ecddd-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ecddd-315">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="ecddd-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ecddd-316">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="ecddd-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-317">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-318">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="ecddd-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ecddd-319">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="ecddd-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ecddd-320">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ecddd-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ecddd-321">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="ecddd-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-323">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="ecddd-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ecddd-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-324">Az.EventHub</span></span>
* <span data-ttu-id="ecddd-325">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ecddd-326">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="ecddd-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ecddd-327">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ecddd-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ecddd-328">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="ecddd-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ecddd-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ecddd-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ecddd-330">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="ecddd-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-331">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-332">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-333">Az.Network</span></span>
* <span data-ttu-id="ecddd-334">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ecddd-335">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="ecddd-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ecddd-336">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="ecddd-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ecddd-337">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="ecddd-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ecddd-338">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="ecddd-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="ecddd-339">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ecddd-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ecddd-340">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ecddd-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-342">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="ecddd-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ecddd-343">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="ecddd-343">Added example</span></span>
    - <span data-ttu-id="ecddd-344">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="ecddd-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ecddd-345">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ecddd-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ecddd-346">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ecddd-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-348">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-349">Az.Resources</span></span>
* <span data-ttu-id="ecddd-350">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ecddd-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ecddd-351">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="ecddd-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ecddd-352">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="ecddd-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ecddd-353">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-354">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-355">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ecddd-356">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="ecddd-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ecddd-357">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="ecddd-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-359">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="ecddd-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ecddd-360">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ecddd-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ecddd-361">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ecddd-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ecddd-362">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="ecddd-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ecddd-363">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ecddd-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ecddd-364">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ecddd-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-365">Az.Sql</span></span>
* <span data-ttu-id="ecddd-366">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ecddd-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-367">Az.Storage</span></span>
* <span data-ttu-id="ecddd-368">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecddd-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ecddd-369">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="ecddd-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ecddd-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ecddd-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ecddd-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ecddd-372">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="ecddd-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ecddd-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ecddd-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-374">Az.Websites</span></span>
* <span data-ttu-id="ecddd-375">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecddd-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ecddd-376">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-377">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-378">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ecddd-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ecddd-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ecddd-380">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="ecddd-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="ecddd-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-381">Az.Automation</span></span>
* <span data-ttu-id="ecddd-382">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="ecddd-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-384">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="ecddd-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-385">Az.Compute</span></span>
* <span data-ttu-id="ecddd-386">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="ecddd-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ecddd-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ecddd-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ecddd-388">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="ecddd-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ecddd-389">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ecddd-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-390">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-391">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="ecddd-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ecddd-392">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="ecddd-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ecddd-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-393">Az.EventHub</span></span>
* <span data-ttu-id="ecddd-394">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ecddd-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ecddd-395">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="ecddd-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ecddd-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-396">Az.KeyVault</span></span>
* <span data-ttu-id="ecddd-397">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="ecddd-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ecddd-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-398">Az.LogicApp</span></span>
* <span data-ttu-id="ecddd-399">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="ecddd-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ecddd-400">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="ecddd-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ecddd-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-401">Az.ManagedServices</span></span>
* <span data-ttu-id="ecddd-402">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="ecddd-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-403">Az.Network</span></span>
* <span data-ttu-id="ecddd-404">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="ecddd-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ecddd-405">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-405">New cmdlets</span></span>
        - <span data-ttu-id="ecddd-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecddd-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ecddd-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ecddd-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ecddd-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ecddd-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ecddd-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ecddd-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ecddd-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ecddd-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ecddd-414">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="ecddd-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ecddd-415">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="ecddd-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ecddd-416">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ecddd-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ecddd-417">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ecddd-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ecddd-418">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="ecddd-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ecddd-419">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="ecddd-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ecddd-420">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="ecddd-420">Updated cmdlets</span></span>
        - <span data-ttu-id="ecddd-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ecddd-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ecddd-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ecddd-424">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ecddd-425">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ecddd-426">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ecddd-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="ecddd-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ecddd-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ecddd-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ecddd-430">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="ecddd-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ecddd-431">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="ecddd-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ecddd-432">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="ecddd-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-434">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="ecddd-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="ecddd-435">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="ecddd-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-437">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ecddd-438">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ecddd-439">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ecddd-440">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ecddd-441">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ecddd-442">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ecddd-443">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ecddd-444">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ecddd-445">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ecddd-446">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ecddd-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-447">Az.Resources</span></span>
- <span data-ttu-id="ecddd-448">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ecddd-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ecddd-449">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ecddd-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-450">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-451">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ecddd-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ecddd-452">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="ecddd-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-453">Az.Sql</span></span>
* <span data-ttu-id="ecddd-454">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ecddd-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ecddd-455">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="ecddd-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ecddd-456">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="ecddd-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-457">Az.Storage</span></span>
* <span data-ttu-id="ecddd-458">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="ecddd-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ecddd-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ecddd-459">Az.StorageSync</span></span>
* <span data-ttu-id="ecddd-460">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ecddd-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ecddd-461">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ecddd-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-462">Az.Websites</span></span>
* <span data-ttu-id="ecddd-463">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ecddd-464">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ecddd-465">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ecddd-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ecddd-466">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-467">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-468">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="ecddd-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ecddd-469">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="ecddd-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ecddd-470">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecddd-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ecddd-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ecddd-471">Az.Advisor</span></span>
* <span data-ttu-id="ecddd-472">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ecddd-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ecddd-473">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="ecddd-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ecddd-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-474">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-475">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ecddd-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ecddd-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ecddd-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ecddd-477">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="ecddd-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ecddd-478">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="ecddd-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ecddd-479">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ecddd-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ecddd-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ecddd-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ecddd-481">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="ecddd-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-482">Az.Automation</span></span>
* <span data-ttu-id="ecddd-483">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ecddd-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-484">Az.Compute</span></span>
* <span data-ttu-id="ecddd-485">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-486">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-487">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="ecddd-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ecddd-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ecddd-488">Az.EventGrid</span></span>
* <span data-ttu-id="ecddd-489">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="ecddd-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-490">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-491">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="ecddd-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-492">Az.Network</span></span>
* <span data-ttu-id="ecddd-493">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="ecddd-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ecddd-494">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="ecddd-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ecddd-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="ecddd-496">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ecddd-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ecddd-497">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ecddd-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-499">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ecddd-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-501">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="ecddd-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-502">Az.Resources</span></span>
    - <span data-ttu-id="ecddd-503">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="ecddd-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ecddd-504">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ecddd-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ecddd-505">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ecddd-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ecddd-506">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="ecddd-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-507">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-508">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ecddd-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-509">Az.Sql</span></span>
* <span data-ttu-id="ecddd-510">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="ecddd-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ecddd-511">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ecddd-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ecddd-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ecddd-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ecddd-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ecddd-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ecddd-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ecddd-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ecddd-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ecddd-518">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="ecddd-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-519">Az.Storage</span></span>
* <span data-ttu-id="ecddd-520">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ecddd-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ecddd-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ecddd-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ecddd-522">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="ecddd-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ecddd-523">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="ecddd-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ecddd-524">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ecddd-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ecddd-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ecddd-527">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="ecddd-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ecddd-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ecddd-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ecddd-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ecddd-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ecddd-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ecddd-530">Az.StorageSync</span></span>
* <span data-ttu-id="ecddd-531">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="ecddd-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ecddd-532">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-533">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-534">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="ecddd-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ecddd-535">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ecddd-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ecddd-536">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="ecddd-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ecddd-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ecddd-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ecddd-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ecddd-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-539">Az.Compute</span></span>
* <span data-ttu-id="ecddd-540">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ecddd-541">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="ecddd-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ecddd-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ecddd-542">Az.Dns</span></span>
* <span data-ttu-id="ecddd-543">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ecddd-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ecddd-544">Az.EventGrid</span></span>
* <span data-ttu-id="ecddd-545">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ecddd-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ecddd-546">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ecddd-546">New cmdlets:</span></span>
    - <span data-ttu-id="ecddd-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ecddd-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ecddd-548">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ecddd-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ecddd-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ecddd-550">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ecddd-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ecddd-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ecddd-552">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ecddd-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ecddd-554">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ecddd-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ecddd-556">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ecddd-557">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ecddd-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ecddd-558">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ecddd-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ecddd-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ecddd-560">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="ecddd-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="ecddd-561">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ecddd-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ecddd-562">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="ecddd-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ecddd-563">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="ecddd-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="ecddd-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ecddd-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ecddd-565">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ecddd-566">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ecddd-567">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="ecddd-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ecddd-568">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="ecddd-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ecddd-569">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="ecddd-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ecddd-570">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ecddd-571">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="ecddd-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ecddd-572">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="ecddd-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="ecddd-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="ecddd-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ecddd-574">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="ecddd-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ecddd-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ecddd-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ecddd-576">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ecddd-577">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ecddd-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ecddd-578">Az.FrontDoor</span></span>
* <span data-ttu-id="ecddd-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ecddd-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ecddd-580">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ecddd-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ecddd-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ecddd-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ecddd-582">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="ecddd-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-583">Az.Network</span></span>
* <span data-ttu-id="ecddd-584">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="ecddd-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ecddd-585">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-585">New cmdlets</span></span>
        - <span data-ttu-id="ecddd-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ecddd-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ecddd-587">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ecddd-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ecddd-588">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-588">New cmdlets</span></span> 
        - <span data-ttu-id="ecddd-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ecddd-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ecddd-590">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ecddd-591">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-591">New cmdlets</span></span> 
        - <span data-ttu-id="ecddd-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="ecddd-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ecddd-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ecddd-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ecddd-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ecddd-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ecddd-597">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecddd-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ecddd-598">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-598">New cmdlets</span></span>
        - <span data-ttu-id="ecddd-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecddd-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ecddd-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecddd-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ecddd-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ecddd-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ecddd-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ecddd-603">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ecddd-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ecddd-604">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="ecddd-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ecddd-605">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="ecddd-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ecddd-606">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ecddd-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ecddd-607">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ecddd-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ecddd-608">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ecddd-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ecddd-609">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ecddd-610">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="ecddd-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ecddd-611">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ecddd-612">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="ecddd-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ecddd-613">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ecddd-614">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ecddd-615">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ecddd-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ecddd-616">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ecddd-617">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="ecddd-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ecddd-618">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="ecddd-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ecddd-619">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="ecddd-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ecddd-620">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="ecddd-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ecddd-621">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ecddd-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="ecddd-622">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ecddd-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="ecddd-623">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ecddd-624">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ecddd-625">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-627">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ecddd-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-628">Az.Resources</span></span>
* <span data-ttu-id="ecddd-629">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="ecddd-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ecddd-630">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ecddd-631">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ecddd-632">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="ecddd-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-634">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="ecddd-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-635">Az.Sql</span></span>
* <span data-ttu-id="ecddd-636">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="ecddd-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ecddd-637">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="ecddd-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ecddd-638">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="ecddd-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ecddd-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ecddd-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ecddd-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ecddd-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ecddd-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ecddd-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ecddd-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ecddd-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-644">Az.Storage</span></span>
* <span data-ttu-id="ecddd-645">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ecddd-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ecddd-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="ecddd-647">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="ecddd-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ecddd-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-649">Az.Websites</span></span>
* <span data-ttu-id="ecddd-650">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="ecddd-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ecddd-651">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ecddd-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ecddd-652">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ecddd-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ecddd-653">Az.Cdn</span></span>
* <span data-ttu-id="ecddd-654">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="ecddd-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-655">Az.Compute</span></span>
* <span data-ttu-id="ecddd-656">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ecddd-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ecddd-657">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ecddd-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ecddd-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-658">Az.EventHub</span></span>
* <span data-ttu-id="ecddd-659">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="ecddd-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ecddd-660">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecddd-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-661">Az.Network</span></span>
* <span data-ttu-id="ecddd-662">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="ecddd-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ecddd-663">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="ecddd-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ecddd-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="ecddd-665">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ecddd-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-667">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="ecddd-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-668">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-669">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecddd-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-671">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ecddd-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ecddd-672">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-673">Az.Sql</span></span>
* <span data-ttu-id="ecddd-674">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ecddd-675">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ecddd-676">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="ecddd-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ecddd-677">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="ecddd-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-678">Az.Websites</span></span>
* <span data-ttu-id="ecddd-679">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="ecddd-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ecddd-680">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ecddd-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-681">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-682">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ecddd-683">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ecddd-684">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ecddd-685">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="ecddd-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ecddd-686">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ecddd-687">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ecddd-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ecddd-688">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ecddd-689">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ecddd-690">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ecddd-691">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="ecddd-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ecddd-692">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ecddd-693">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="ecddd-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ecddd-694">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="ecddd-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ecddd-695">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="ecddd-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ecddd-696">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="ecddd-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ecddd-697">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="ecddd-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ecddd-698">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="ecddd-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ecddd-699">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="ecddd-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ecddd-700">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="ecddd-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="ecddd-701">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="ecddd-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ecddd-702">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="ecddd-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ecddd-703">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="ecddd-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ecddd-704">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="ecddd-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ecddd-705">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="ecddd-706">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="ecddd-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ecddd-707">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="ecddd-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ecddd-708">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ecddd-709">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ecddd-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ecddd-710">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ecddd-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ecddd-711">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="ecddd-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ecddd-712">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="ecddd-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="ecddd-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ecddd-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ecddd-714">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ecddd-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ecddd-715">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ecddd-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ecddd-716">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ecddd-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ecddd-717">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="ecddd-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ecddd-718">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="ecddd-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ecddd-719">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="ecddd-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ecddd-720">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="ecddd-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ecddd-721">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ecddd-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="ecddd-722">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ecddd-723">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ecddd-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ecddd-724">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ecddd-725">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="ecddd-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ecddd-726">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ecddd-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ecddd-727">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ecddd-728">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ecddd-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="ecddd-729">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="ecddd-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ecddd-730">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ecddd-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ecddd-731">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ecddd-732">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="ecddd-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ecddd-733">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ecddd-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ecddd-734">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="ecddd-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ecddd-735">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ecddd-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ecddd-736">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="ecddd-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ecddd-737">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ecddd-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ecddd-738">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ecddd-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ecddd-739">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ecddd-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ecddd-740">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ecddd-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ecddd-741">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ecddd-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ecddd-742">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ecddd-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ecddd-743">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ecddd-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ecddd-744">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ecddd-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ecddd-745">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ecddd-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ecddd-746">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="ecddd-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ecddd-747">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ecddd-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ecddd-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ecddd-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ecddd-749">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ecddd-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ecddd-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ecddd-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ecddd-751">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ecddd-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ecddd-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ecddd-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ecddd-753">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ecddd-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ecddd-754">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ecddd-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ecddd-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ecddd-756">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ecddd-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="ecddd-757">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ecddd-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ecddd-758">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ecddd-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-759">Az.Automation</span></span>
* <span data-ttu-id="ecddd-760">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="ecddd-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ecddd-761">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ecddd-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ecddd-762">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ecddd-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ecddd-763">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="ecddd-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ecddd-764">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ecddd-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ecddd-765">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="ecddd-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ecddd-766">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="ecddd-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-767">Az.Compute</span></span>
* <span data-ttu-id="ecddd-768">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ecddd-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ecddd-769">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="ecddd-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-771">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-772">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-773">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-774">Az.Network</span></span>
* <span data-ttu-id="ecddd-775">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="ecddd-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ecddd-776">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ecddd-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="ecddd-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ecddd-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ecddd-778">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ecddd-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-779">Az.Resources</span></span>
* <span data-ttu-id="ecddd-780">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="ecddd-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-781">Az.Sql</span></span>
* <span data-ttu-id="ecddd-782">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="ecddd-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ecddd-783">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-784">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-785">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="ecddd-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-787">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="ecddd-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ecddd-788">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="ecddd-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-789">Az.Compute</span></span>
* <span data-ttu-id="ecddd-790">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="ecddd-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ecddd-791">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ecddd-792">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ecddd-793">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ecddd-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ecddd-794">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ecddd-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ecddd-795">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecddd-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="ecddd-796">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="ecddd-796">Breaking changes</span></span>
    - <span data-ttu-id="ecddd-797">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ecddd-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ecddd-798">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ecddd-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ecddd-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ecddd-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="ecddd-800">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ecddd-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ecddd-801">Az.Dns</span></span>
* <span data-ttu-id="ecddd-802">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="ecddd-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ecddd-803">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="ecddd-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ecddd-804">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ecddd-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ecddd-805">Az.FrontDoor</span></span>
* <span data-ttu-id="ecddd-806">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ecddd-807">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ecddd-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ecddd-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ecddd-808">Az.HDInsight</span></span>
* <span data-ttu-id="ecddd-809">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ecddd-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ecddd-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ecddd-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ecddd-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ecddd-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ecddd-812">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ecddd-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ecddd-813">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="ecddd-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ecddd-814">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="ecddd-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ecddd-815">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="ecddd-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-816">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-817">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="ecddd-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="ecddd-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ecddd-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ecddd-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ecddd-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ecddd-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ecddd-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ecddd-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ecddd-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ecddd-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ecddd-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ecddd-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ecddd-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ecddd-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ecddd-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ecddd-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ecddd-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ecddd-829">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="ecddd-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ecddd-830">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="ecddd-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-831">Az.Network</span></span>
* <span data-ttu-id="ecddd-832">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="ecddd-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ecddd-833">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecddd-833">New cmdlets</span></span>
        - <span data-ttu-id="ecddd-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="ecddd-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ecddd-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ecddd-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ecddd-838">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="ecddd-838">Updated cmdlets</span></span>
        - <span data-ttu-id="ecddd-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ecddd-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ecddd-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ecddd-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ecddd-841">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="ecddd-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ecddd-842">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ecddd-843">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="ecddd-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ecddd-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="ecddd-845">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="ecddd-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ecddd-846">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ecddd-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ecddd-847">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-849">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ecddd-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ecddd-850">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ecddd-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ecddd-851">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ecddd-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ecddd-852">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ecddd-853">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ecddd-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ecddd-854">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="ecddd-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ecddd-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ecddd-855">Az.Relay</span></span>
* <span data-ttu-id="ecddd-856">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="ecddd-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-857">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-858">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="ecddd-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-859">Az.Storage</span></span>
* <span data-ttu-id="ecddd-860">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ecddd-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ecddd-861">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="ecddd-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ecddd-862">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ecddd-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ecddd-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="ecddd-864">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ecddd-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ecddd-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ecddd-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ecddd-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-868">Az.Websites</span></span>
* <span data-ttu-id="ecddd-869">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ecddd-870">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="ecddd-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ecddd-871">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ecddd-872">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="ecddd-872">Highlights since the last major release</span></span>
* <span data-ttu-id="ecddd-873">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ecddd-873">General availability of `Az` module</span></span>
* <span data-ttu-id="ecddd-874">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ecddd-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ecddd-875">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ecddd-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ecddd-876">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ecddd-877">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ecddd-878">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ecddd-879">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="ecddd-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ecddd-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-880">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-881">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="ecddd-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ecddd-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ecddd-882">Az.Batch</span></span>
* <span data-ttu-id="ecddd-883">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ecddd-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ecddd-884">Az.Cdn</span></span>
* <span data-ttu-id="ecddd-885">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-887">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-888">Az.Compute</span></span>
* <span data-ttu-id="ecddd-889">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="ecddd-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ecddd-890">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-891">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="ecddd-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-892">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-893">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ecddd-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-895">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ecddd-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ecddd-896">Az.EventGrid</span></span>
* <span data-ttu-id="ecddd-897">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="ecddd-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ecddd-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-898">Az.EventHub</span></span>
* <span data-ttu-id="ecddd-899">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="ecddd-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="ecddd-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ecddd-900">Az.HDInsight</span></span>
* <span data-ttu-id="ecddd-901">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-902">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-903">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ecddd-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-904">Az.KeyVault</span></span>
* <span data-ttu-id="ecddd-905">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-906">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="ecddd-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ecddd-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ecddd-907">Az.MachineLearning</span></span>
* <span data-ttu-id="ecddd-908">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ecddd-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ecddd-909">Az.Media</span></span>
* <span data-ttu-id="ecddd-910">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-911">Az.Monitor</span></span>
  * <span data-ttu-id="ecddd-912">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="ecddd-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ecddd-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ecddd-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ecddd-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ecddd-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ecddd-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ecddd-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ecddd-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ecddd-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ecddd-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ecddd-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ecddd-918">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ecddd-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-919">Az.Network</span></span>
* <span data-ttu-id="ecddd-920">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-921">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="ecddd-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ecddd-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ecddd-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="ecddd-923">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-925">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ecddd-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ecddd-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ecddd-927">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-929">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-930">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ecddd-931">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ecddd-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ecddd-932">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="ecddd-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ecddd-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ecddd-933">Az.RedisCache</span></span>
* <span data-ttu-id="ecddd-934">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-935">Az.Resources</span></span>
* <span data-ttu-id="ecddd-936">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="ecddd-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-937">Az.Sql</span></span>
* <span data-ttu-id="ecddd-938">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="ecddd-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ecddd-939">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-940">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="ecddd-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ecddd-941">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="ecddd-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ecddd-942">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="ecddd-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ecddd-943">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ecddd-944">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="ecddd-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-945">Az.Websites</span></span>
* <span data-ttu-id="ecddd-946">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="ecddd-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ecddd-947">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ecddd-948">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="ecddd-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ecddd-949">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ecddd-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ecddd-950">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ecddd-951">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="ecddd-951">Highlights since the last major release</span></span>
* <span data-ttu-id="ecddd-952">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ecddd-952">General availability of `Az` module</span></span>
* <span data-ttu-id="ecddd-953">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ecddd-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ecddd-954">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ecddd-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ecddd-955">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ecddd-956">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ecddd-957">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ecddd-958">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="ecddd-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ecddd-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-959">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-960">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ecddd-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ecddd-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="ecddd-962">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="ecddd-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ecddd-963">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="ecddd-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-964">Az.Automation</span></span>
* <span data-ttu-id="ecddd-965">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="ecddd-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ecddd-966">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="ecddd-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ecddd-967">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-968">Az.Compute</span></span>
* <span data-ttu-id="ecddd-969">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ecddd-970">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="ecddd-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ecddd-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="ecddd-972">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="ecddd-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-973">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-974">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ecddd-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ecddd-975">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ecddd-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-976">Az.Resources</span></span>
* <span data-ttu-id="ecddd-977">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="ecddd-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ecddd-978">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ecddd-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ecddd-979">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="ecddd-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ecddd-980">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ecddd-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ecddd-981">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="ecddd-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ecddd-982">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ecddd-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-983">Az.Sql</span></span>
* <span data-ttu-id="ecddd-984">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="ecddd-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-985">Az.Storage</span></span>
* <span data-ttu-id="ecddd-986">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ecddd-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecddd-987">New-AzStorageContext</span></span>
* <span data-ttu-id="ecddd-988">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ecddd-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ecddd-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ecddd-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ecddd-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ecddd-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ecddd-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ecddd-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ecddd-993">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="ecddd-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ecddd-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ecddd-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ecddd-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ecddd-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ecddd-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ecddd-998">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ecddd-999">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="ecddd-999">Highlights since the last major release</span></span>
* <span data-ttu-id="ecddd-1000">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ecddd-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="ecddd-1001">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ecddd-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ecddd-1002">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ecddd-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ecddd-1003">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ecddd-1004">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ecddd-1005">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ecddd-1006">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="ecddd-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1007">Az.Automation</span></span>
* <span data-ttu-id="ecddd-1008">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="ecddd-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ecddd-1009">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="ecddd-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="ecddd-1010">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="ecddd-1010">Pre-Post script</span></span>
    * <span data-ttu-id="ecddd-1011">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="ecddd-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1012">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1013">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ecddd-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ecddd-1014">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ecddd-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-1015">Az.KeyVault</span></span>
* <span data-ttu-id="ecddd-1016">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1017">Az.Network</span></span>
* <span data-ttu-id="ecddd-1018">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ecddd-1019">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="ecddd-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-1021">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ecddd-1022">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="ecddd-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1023">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1024">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecddd-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ecddd-1025">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="ecddd-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1026">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1027">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1028">Az.Storage</span></span>
* <span data-ttu-id="ecddd-1029">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="ecddd-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ecddd-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ecddd-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ecddd-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ecddd-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ecddd-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ecddd-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ecddd-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ecddd-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1036">Az.Websites</span></span>
* <span data-ttu-id="ecddd-1037">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="ecddd-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ecddd-1038">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1039">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-1040">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="ecddd-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ecddd-1041">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1042">Az.Automation</span></span>
* <span data-ttu-id="ecddd-1043">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ecddd-1044">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ecddd-1045">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="ecddd-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ecddd-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ecddd-1046">Az.Cdn</span></span>
* <span data-ttu-id="ecddd-1047">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1048">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1049">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="ecddd-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-1050">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-1051">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ecddd-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-1052">Az.LogicApp</span></span>
* <span data-ttu-id="ecddd-1053">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1054">Az.Network</span></span>
* <span data-ttu-id="ecddd-1055">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-1057">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ecddd-1058">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="ecddd-1058">SDK Update</span></span>
* <span data-ttu-id="ecddd-1059">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ecddd-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ecddd-1060">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ecddd-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1061">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1062">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="ecddd-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ecddd-1063">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ecddd-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ecddd-1064">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ecddd-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ecddd-1065">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ecddd-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ecddd-1066">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ecddd-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ecddd-1067">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ecddd-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1068">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1069">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ecddd-1070">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1071">Az.Storage</span></span>
* <span data-ttu-id="ecddd-1072">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ecddd-1073">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ecddd-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="ecddd-1075">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1076">Az.Automation</span></span>
* <span data-ttu-id="ecddd-1077">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ecddd-1078">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ecddd-1079">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-1081">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1082">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1083">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="ecddd-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ecddd-1084">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="ecddd-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ecddd-1085">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ecddd-1086">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-1088">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ecddd-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-1089">Az.EventHub</span></span>
* <span data-ttu-id="ecddd-1090">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ecddd-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-1091">Az.KeyVault</span></span>
* <span data-ttu-id="ecddd-1092">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ecddd-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ecddd-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-1093">Az.LogicApp</span></span>
* <span data-ttu-id="ecddd-1094">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="ecddd-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ecddd-1095">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="ecddd-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ecddd-1096">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="ecddd-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ecddd-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ecddd-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ecddd-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ecddd-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ecddd-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ecddd-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ecddd-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ecddd-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ecddd-1101">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="ecddd-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ecddd-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ecddd-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ecddd-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ecddd-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ecddd-1106">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ecddd-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-1107">Az.Monitor</span></span>
* <span data-ttu-id="ecddd-1108">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ecddd-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1109">Az.Network</span></span>
* <span data-ttu-id="ecddd-1110">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ecddd-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="ecddd-1112">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ecddd-1113">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ecddd-1114">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ecddd-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1115">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1116">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ecddd-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ecddd-1117">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ecddd-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ecddd-1118">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ecddd-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ecddd-1119">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ecddd-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1120">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1121">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ecddd-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ecddd-1122">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="ecddd-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1123">Az.Websites</span></span>
* <span data-ttu-id="ecddd-1124">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ecddd-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ecddd-1125">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1126">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-1127">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ecddd-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ecddd-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="ecddd-1129">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1130">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1131">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="ecddd-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ecddd-1132">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ecddd-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ecddd-1133">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="ecddd-1135">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1136">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1137">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ecddd-1138">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ecddd-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ecddd-1139">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ecddd-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ecddd-1140">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ecddd-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1141">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1142">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ecddd-1143">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="ecddd-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ecddd-1144">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ecddd-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ecddd-1145">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1146">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-1147">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="ecddd-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ecddd-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="ecddd-1149">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="ecddd-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="ecddd-1151">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="ecddd-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ecddd-1152">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1153">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-1154">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ecddd-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ecddd-1155">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ecddd-1156">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ecddd-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ecddd-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ecddd-1157">Az.Aks</span></span>
* <span data-ttu-id="ecddd-1158">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ecddd-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1159">Az.Automation</span></span>
* <span data-ttu-id="ecddd-1160">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="ecddd-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ecddd-1161">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ecddd-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ecddd-1162">Az.Cdn</span></span>
* <span data-ttu-id="ecddd-1163">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1164">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1165">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ecddd-1166">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ecddd-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ecddd-1167">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ecddd-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ecddd-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ecddd-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ecddd-1169">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ecddd-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecddd-1170">Az.DataFactory</span></span>
* <span data-ttu-id="ecddd-1171">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ecddd-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-1173">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="ecddd-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ecddd-1174">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ecddd-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ecddd-1175">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-1176">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-1177">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ecddd-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-1178">Az.KeyVault</span></span>
* <span data-ttu-id="ecddd-1179">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1180">Az.Network</span></span>
* <span data-ttu-id="ecddd-1181">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1182">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1183">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="ecddd-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ecddd-1184">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ecddd-1185">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ecddd-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ecddd-1186">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ecddd-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ecddd-1187">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ecddd-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ecddd-1188">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ecddd-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ecddd-1189">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ecddd-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-1191">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ecddd-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ecddd-1192">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1192">Fix some error messages.</span></span>
* <span data-ttu-id="ecddd-1193">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ecddd-1194">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ecddd-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ecddd-1195">Az.SignalR</span></span>
* <span data-ttu-id="ecddd-1196">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1197">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1198">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ecddd-1199">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="ecddd-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ecddd-1200">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="ecddd-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ecddd-1201">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="ecddd-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1202">Az.Storage</span></span>
* <span data-ttu-id="ecddd-1203">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ecddd-1204">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ecddd-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ecddd-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ecddd-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ecddd-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ecddd-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ecddd-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="ecddd-1208">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1209">Az.Websites</span></span>
* <span data-ttu-id="ecddd-1210">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="ecddd-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ecddd-1211">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ecddd-1212">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ecddd-1213">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="ecddd-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ecddd-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1214">Az.Accounts</span></span>
* <span data-ttu-id="ecddd-1215">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ecddd-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1216">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1217">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ecddd-1218">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="ecddd-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ecddd-1219">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-1221">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ecddd-1222">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="ecddd-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ecddd-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ecddd-1223">Az.EventGrid</span></span>
* <span data-ttu-id="ecddd-1224">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ecddd-1225">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ecddd-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ecddd-1226">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="ecddd-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ecddd-1227">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="ecddd-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ecddd-1228">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ecddd-1229">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="ecddd-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ecddd-1230">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="ecddd-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ecddd-1231">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="ecddd-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ecddd-1232">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ecddd-1233">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="ecddd-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="ecddd-1234">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ecddd-1235">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ecddd-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-1236">Az.IotHub</span></span>
* <span data-ttu-id="ecddd-1237">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="ecddd-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ecddd-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ecddd-1238">Az.LogicApp</span></span>
* <span data-ttu-id="ecddd-1239">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="ecddd-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1240">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1241">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ecddd-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ecddd-1242">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ecddd-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ecddd-1243">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecddd-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ecddd-1244">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ecddd-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ecddd-1245">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="ecddd-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ecddd-1246">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ecddd-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ecddd-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ecddd-1247">Az.SignalR</span></span>
* <span data-ttu-id="ecddd-1248">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1249">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1250">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ecddd-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1251">Az.Storage</span></span>
* <span data-ttu-id="ecddd-1252">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="ecddd-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ecddd-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecddd-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="ecddd-1254">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ecddd-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ecddd-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1256">Az.Websites</span></span>
* <span data-ttu-id="ecddd-1257">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="ecddd-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ecddd-1258">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ecddd-1259">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ecddd-1260">Geral</span><span class="sxs-lookup"><span data-stu-id="ecddd-1260">General</span></span>

- <span data-ttu-id="ecddd-1261">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="ecddd-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="ecddd-1262">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1262">Online help for each module</span></span>
- <span data-ttu-id="ecddd-1263">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ecddd-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ecddd-1264">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="ecddd-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ecddd-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1265">Az.Accounts</span></span>
- <span data-ttu-id="ecddd-1266">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="ecddd-1267">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="ecddd-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ecddd-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="ecddd-1269">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="ecddd-1269">Fixes for #7002</span></span>
- <span data-ttu-id="ecddd-1270">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ecddd-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ecddd-1271">Az.Batch</span></span>
- <span data-ttu-id="ecddd-1272">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ecddd-1273">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ecddd-1274">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ecddd-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ecddd-1275">Az.Billing</span></span>
- <span data-ttu-id="ecddd-1276">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ecddd-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="ecddd-1278">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ecddd-1279">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ecddd-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ecddd-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="ecddd-1281">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ecddd-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ecddd-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ecddd-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ecddd-1283">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="ecddd-1285">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ecddd-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ecddd-1286">Az.Monitor</span></span>
- <span data-ttu-id="ecddd-1287">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ecddd-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ecddd-1288">Az.KeyVault</span></span>
- <span data-ttu-id="ecddd-1289">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="ecddd-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ecddd-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ecddd-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="ecddd-1291">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ecddd-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ecddd-1292">Az.Media</span></span>
- <span data-ttu-id="ecddd-1293">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ecddd-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ecddd-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1294">Az.Network</span></span>
<span data-ttu-id="ecddd-1295">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ecddd-1296">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="ecddd-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="ecddd-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ecddd-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ecddd-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ecddd-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ecddd-1305">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ecddd-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ecddd-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ecddd-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ecddd-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ecddd-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ecddd-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ecddd-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ecddd-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ecddd-1312">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ecddd-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ecddd-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ecddd-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ecddd-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ecddd-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ecddd-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ecddd-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ecddd-1316">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ecddd-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ecddd-1317">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ecddd-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="ecddd-1319">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ecddd-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1320">Az.Profile</span></span>
- <span data-ttu-id="ecddd-1321">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ecddd-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="ecddd-1323">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ecddd-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1324">Az.Resources</span></span>
- <span data-ttu-id="ecddd-1325">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ecddd-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="ecddd-1327">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="ecddd-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ecddd-1328">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ecddd-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ecddd-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="ecddd-1330">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ecddd-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ecddd-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1331">Az.Sql</span></span>
- <span data-ttu-id="ecddd-1332">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="ecddd-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ecddd-1333">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="ecddd-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ecddd-1334">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ecddd-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1335">Az.Storage</span></span>
- <span data-ttu-id="ecddd-1336">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ecddd-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1337">Az.Websites</span></span>
- <span data-ttu-id="ecddd-1338">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="ecddd-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ecddd-1339">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ecddd-1340">Geral</span><span class="sxs-lookup"><span data-stu-id="ecddd-1340">General</span></span>

* <span data-ttu-id="ecddd-1341">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="ecddd-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ecddd-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1342">Az.Compute</span></span>

* <span data-ttu-id="ecddd-1343">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="ecddd-1345">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="ecddd-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ecddd-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ecddd-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="ecddd-1347">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="ecddd-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="ecddd-1348">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ecddd-1349">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ecddd-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="ecddd-1351">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ecddd-1352">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ecddd-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1353">Az.Resources</span></span>

* <span data-ttu-id="ecddd-1354">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ecddd-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ecddd-1355">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ecddd-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1356">Az.Sql</span></span>

* <span data-ttu-id="ecddd-1357">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="ecddd-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ecddd-1358">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="ecddd-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ecddd-1359">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ecddd-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1360">Az.Storage</span></span>

* <span data-ttu-id="ecddd-1361">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ecddd-1362">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="ecddd-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ecddd-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ecddd-1364">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="ecddd-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="ecddd-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ecddd-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ecddd-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ecddd-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ecddd-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1367">Az.Websites</span></span>

* <span data-ttu-id="ecddd-1368">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ecddd-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ecddd-1369">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ecddd-1370">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ecddd-1371">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ecddd-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ecddd-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="ecddd-1373">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ecddd-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ecddd-1374">Az.Automation</span></span>
* <span data-ttu-id="ecddd-1375">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="ecddd-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ecddd-1376">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ecddd-1377">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ecddd-1378">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="ecddd-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ecddd-1379">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="ecddd-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ecddd-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1380">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1381">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ecddd-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ecddd-1382">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ecddd-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="ecddd-1384">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ecddd-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ecddd-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ecddd-1386">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="ecddd-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ecddd-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1387">Az.Network</span></span>
* <span data-ttu-id="ecddd-1388">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ecddd-1389">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="ecddd-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ecddd-1390">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ecddd-1391">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ecddd-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ecddd-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ecddd-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ecddd-1393">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ecddd-1394">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ecddd-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ecddd-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ecddd-1396">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ecddd-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ecddd-1397">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="ecddd-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ecddd-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ecddd-1398">Az.Relay</span></span>
* <span data-ttu-id="ecddd-1399">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ecddd-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1400">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1401">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ecddd-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ecddd-1402">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="ecddd-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ecddd-1403">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ecddd-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ecddd-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-1405">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="ecddd-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ecddd-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1406">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1407">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="ecddd-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ecddd-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ecddd-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ecddd-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ecddd-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ecddd-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ecddd-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ecddd-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ecddd-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ecddd-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ecddd-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ecddd-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ecddd-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ecddd-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ecddd-1416">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ecddd-1417">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ecddd-1418">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ecddd-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ecddd-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ecddd-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ecddd-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ecddd-1423">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ecddd-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ecddd-1424">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ecddd-1425">Geral</span><span class="sxs-lookup"><span data-stu-id="ecddd-1425">General</span></span>
* <span data-ttu-id="ecddd-1426">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="ecddd-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ecddd-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1427">Az.Profile</span></span>
* <span data-ttu-id="ecddd-1428">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ecddd-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ecddd-1429">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="ecddd-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ecddd-1430">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ecddd-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ecddd-1431">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="ecddd-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ecddd-1432">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="ecddd-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ecddd-1433">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="ecddd-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ecddd-1434">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="ecddd-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-1436">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1437">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1438">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ecddd-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ecddd-1439">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ecddd-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ecddd-1440">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-1442">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ecddd-1443">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ecddd-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ecddd-1444">Az.Insights</span></span>
* <span data-ttu-id="ecddd-1445">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="ecddd-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ecddd-1446">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="ecddd-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ecddd-1447">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="ecddd-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ecddd-1448">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="ecddd-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1449">Az.Network</span></span>
* <span data-ttu-id="ecddd-1450">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="ecddd-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ecddd-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ecddd-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ecddd-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ecddd-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ecddd-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ecddd-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ecddd-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ecddd-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ecddd-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ecddd-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ecddd-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ecddd-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ecddd-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ecddd-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="ecddd-1458">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="ecddd-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1459">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1460">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ecddd-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ecddd-1461">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="ecddd-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ecddd-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ecddd-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="ecddd-1463">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ecddd-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ecddd-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="ecddd-1465">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ecddd-1466">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="ecddd-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ecddd-1467">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ecddd-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ecddd-1468">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ecddd-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ecddd-1469">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ecddd-1470">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ecddd-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1471">Az.Profile</span></span>
* <span data-ttu-id="ecddd-1472">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="ecddd-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ecddd-1473">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ecddd-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1474">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1475">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="ecddd-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ecddd-1476">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ecddd-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ecddd-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="ecddd-1478">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="ecddd-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ecddd-1479">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ecddd-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ecddd-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ecddd-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1483">Az.Network</span></span>
* <span data-ttu-id="ecddd-1484">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ecddd-1485">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1486">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1487">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ecddd-1488">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ecddd-1489">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ecddd-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1490">Azure.Storage</span></span>
* <span data-ttu-id="ecddd-1491">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ecddd-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ecddd-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ecddd-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ecddd-1494">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ecddd-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ecddd-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ecddd-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ecddd-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="ecddd-1497">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ecddd-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ecddd-1498">Az.Compute</span></span>
* <span data-ttu-id="ecddd-1499">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="ecddd-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ecddd-1500">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ecddd-1501">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="ecddd-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ecddd-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ecddd-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ecddd-1503">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ecddd-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ecddd-1504">Az.Network</span></span>
* <span data-ttu-id="ecddd-1505">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ecddd-1506">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="ecddd-1506">new cmdlets added</span></span>
    - <span data-ttu-id="ecddd-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ecddd-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ecddd-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ecddd-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ecddd-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ecddd-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ecddd-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ecddd-1513">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="ecddd-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ecddd-1514">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ecddd-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ecddd-1515">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ecddd-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ecddd-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ecddd-1516">Az.RedisCache</span></span>
* <span data-ttu-id="ecddd-1517">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="ecddd-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ecddd-1518">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ecddd-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ecddd-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ecddd-1519">Az.Resources</span></span>
* <span data-ttu-id="ecddd-1520">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ecddd-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ecddd-1521">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="ecddd-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ecddd-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ecddd-1522">Az.Sql</span></span>
* <span data-ttu-id="ecddd-1523">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="ecddd-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ecddd-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ecddd-1524">Az.Websites</span></span>
* <span data-ttu-id="ecddd-1525">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="ecddd-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ecddd-1526">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="ecddd-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ecddd-1527">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="ecddd-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ecddd-1528">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="ecddd-1528">Initial Release</span></span>
