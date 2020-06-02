---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: bcbb78809c2db63d665dc0c3d05e0614acce6045
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122150"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="11563-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="11563-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="11563-104">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="11563-105">Geral</span><span class="sxs-lookup"><span data-stu-id="11563-105">General</span></span>
* <span data-ttu-id="11563-106">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11563-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11563-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-107">Az.Accounts</span></span>
* <span data-ttu-id="11563-108">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="11563-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11563-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-109">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-110">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="11563-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="11563-111">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="11563-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-112">Az.Automation</span></span>
* <span data-ttu-id="11563-113">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="11563-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11563-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11563-114">Az.Batch</span></span>
* <span data-ttu-id="11563-115">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="11563-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-116">Az.Compute</span></span>
* <span data-ttu-id="11563-117">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11563-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="11563-118">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="11563-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="11563-119">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="11563-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="11563-120">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="11563-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-121">Az.DataFactory</span></span>
* <span data-ttu-id="11563-122">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="11563-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="11563-123">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="11563-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="11563-124">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="11563-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-126">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="11563-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="11563-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="11563-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="11563-128">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="11563-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="11563-129">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="11563-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="11563-130">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="11563-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="11563-131">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="11563-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-132">Az.IotHub</span></span>
* <span data-ttu-id="11563-133">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="11563-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="11563-134">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="11563-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-135">Az.Monitor</span></span>
* <span data-ttu-id="11563-136">Novos receptores do grupo de ações adicionados ao New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="11563-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="11563-137">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="11563-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="11563-138">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="11563-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="11563-139">Agora os Webhooks oferecem suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="11563-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-140">Az.Network</span></span>
* <span data-ttu-id="11563-141">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="11563-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="11563-142">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11563-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="11563-143">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11563-143">New cmdlets added:</span></span>
        - <span data-ttu-id="11563-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="11563-145">Cmdlets atualizados com o parâmetro opcional -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="11563-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="11563-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11563-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="11563-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11563-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11563-148">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="11563-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="11563-149">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="11563-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="11563-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11563-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11563-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11563-153">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="11563-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="11563-154">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="11563-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="11563-155">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="11563-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="11563-156">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="11563-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11563-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11563-157">Az.RedisCache</span></span>
* <span data-ttu-id="11563-158">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="11563-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-159">Az.Sql</span></span>
* <span data-ttu-id="11563-160">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="11563-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-161">Az.Storage</span></span>
* <span data-ttu-id="11563-162">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="11563-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="11563-163">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="11563-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11563-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="11563-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="11563-165">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="11563-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="11563-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11563-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11563-167">Az.StorageSync</span></span>
* <span data-ttu-id="11563-168">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="11563-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-169">Az.Websites</span></span>
* <span data-ttu-id="11563-170">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="11563-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="11563-171">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11563-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-172">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-173">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="11563-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="11563-174">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="11563-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="11563-175">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="11563-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-176">Az.Automation</span></span>
* <span data-ttu-id="11563-177">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="11563-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="11563-178">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="11563-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="11563-179">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="11563-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-180">Az.Compute</span></span>
* <span data-ttu-id="11563-181">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="11563-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="11563-182">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11563-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11563-183">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="11563-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="11563-184">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="11563-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="11563-185">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="11563-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="11563-186">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="11563-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="11563-187">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="11563-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="11563-188">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="11563-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="11563-189">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="11563-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-190">Az.DataFactory</span></span>
* <span data-ttu-id="11563-191">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="11563-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="11563-192">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="11563-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11563-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11563-193">Az.HDInsight</span></span>
* <span data-ttu-id="11563-194">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="11563-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-195">Az.IotHub</span></span>
* <span data-ttu-id="11563-196">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="11563-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="11563-197">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="11563-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="11563-198">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="11563-198">New cmdlets are:</span></span>
    - <span data-ttu-id="11563-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11563-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11563-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11563-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11563-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11563-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="11563-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="11563-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-203">Az.Monitor</span></span>
* <span data-ttu-id="11563-204">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="11563-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="11563-205">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="11563-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="11563-206">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="11563-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="11563-207">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="11563-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="11563-208">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="11563-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="11563-209">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="11563-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="11563-210">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11563-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="11563-211">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="11563-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="11563-212">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="11563-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11563-213">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="11563-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="11563-214">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="11563-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="11563-215">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="11563-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="11563-216">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="11563-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="11563-217">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="11563-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="11563-218">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="11563-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="11563-219">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="11563-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="11563-220">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="11563-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="11563-221">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="11563-222">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="11563-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="11563-223">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-223">Overall improved help files</span></span>
* <span data-ttu-id="11563-224">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="11563-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-225">Az.Network</span></span>
* <span data-ttu-id="11563-226">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="11563-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="11563-227">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="11563-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="11563-228">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="11563-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="11563-229">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="11563-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="11563-230">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="11563-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="11563-231">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="11563-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="11563-232">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="11563-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="11563-233">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="11563-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="11563-234">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="11563-235">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="11563-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="11563-236">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="11563-237">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="11563-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="11563-238">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-238">New cmdlets</span></span>
        - <span data-ttu-id="11563-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="11563-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="11563-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="11563-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="11563-241">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11563-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="11563-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11563-242">New-VpnSite</span></span>
        - <span data-ttu-id="11563-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="11563-243">Update-VpnSite</span></span>
        - <span data-ttu-id="11563-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11563-244">New-VpnConnection</span></span>
        - <span data-ttu-id="11563-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11563-245">Update-VpnConnection</span></span>
* <span data-ttu-id="11563-246">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="11563-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-248">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="11563-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="11563-249">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="11563-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-250">Az.Resources</span></span>
* <span data-ttu-id="11563-251">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="11563-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-253">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="11563-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="11563-254">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="11563-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="11563-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11563-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11563-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11563-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11563-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11563-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11563-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11563-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="11563-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11563-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11563-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11563-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11563-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11563-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11563-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11563-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11563-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="11563-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="11563-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="11563-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="11563-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="11563-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="11563-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11563-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="11563-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="11563-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="11563-268">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="11563-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11563-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11563-269">Az.SignalR</span></span>
* <span data-ttu-id="11563-270">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="11563-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-271">Az.Sql</span></span>
* <span data-ttu-id="11563-272">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="11563-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="11563-273">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="11563-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="11563-274">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="11563-275">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="11563-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="11563-276">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="11563-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-277">Az.Storage</span></span>
* <span data-ttu-id="11563-278">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="11563-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="11563-279">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="11563-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="11563-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11563-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="11563-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11563-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="11563-282">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="11563-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="11563-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11563-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="11563-284">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="11563-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="11563-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11563-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11563-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11563-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11563-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11563-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="11563-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="11563-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-289">Az.Websites</span></span>
* <span data-ttu-id="11563-290">Corrigindo o problema em que as marcas webapp eram excluídas ao migrar o aplicativo para o novo ASP</span><span class="sxs-lookup"><span data-stu-id="11563-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="11563-291">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="11563-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="11563-292">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="11563-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="11563-293">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="11563-294">Geral</span><span class="sxs-lookup"><span data-stu-id="11563-294">General</span></span>
* <span data-ttu-id="11563-295">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="11563-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11563-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-296">Az.Accounts</span></span>
* <span data-ttu-id="11563-297">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="11563-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="11563-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11563-298">Az.Aks</span></span>
* <span data-ttu-id="11563-299">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="11563-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="11563-300">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="11563-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11563-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-301">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-302">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="11563-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="11563-303">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="11563-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="11563-304">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="11563-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="11563-305">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="11563-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="11563-306">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11563-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11563-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11563-307">Az.Batch</span></span>
* <span data-ttu-id="11563-308">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="11563-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11563-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11563-309">Az.Cdn</span></span>
* <span data-ttu-id="11563-310">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="11563-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-311">Az.Compute</span></span>
* <span data-ttu-id="11563-312">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="11563-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="11563-313">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11563-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="11563-314">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="11563-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="11563-315">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="11563-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="11563-316">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="11563-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="11563-317">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="11563-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="11563-318">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="11563-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="11563-319">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="11563-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-320">Az.DataFactory</span></span>
* <span data-ttu-id="11563-321">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="11563-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="11563-322">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="11563-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="11563-323">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="11563-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="11563-324">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="11563-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-326">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="11563-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11563-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-327">Az.EventHub</span></span>
* <span data-ttu-id="11563-328">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="11563-329">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="11563-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="11563-330">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="11563-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="11563-331">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="11563-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="11563-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11563-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11563-333">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="11563-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-334">Az.Monitor</span></span>
* <span data-ttu-id="11563-335">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-336">Az.Network</span></span>
* <span data-ttu-id="11563-337">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="11563-338">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="11563-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="11563-339">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="11563-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="11563-340">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="11563-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="11563-341">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="11563-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="11563-342">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11563-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="11563-343">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="11563-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-345">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="11563-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="11563-346">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="11563-346">Added example</span></span>
    - <span data-ttu-id="11563-347">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="11563-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="11563-348">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="11563-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="11563-349">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="11563-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-351">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="11563-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-352">Az.Resources</span></span>
* <span data-ttu-id="11563-353">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="11563-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="11563-354">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="11563-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="11563-355">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="11563-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="11563-356">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-357">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-358">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="11563-359">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="11563-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="11563-360">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="11563-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-362">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="11563-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="11563-363">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="11563-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="11563-364">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="11563-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="11563-365">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="11563-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="11563-366">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="11563-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="11563-367">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="11563-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-368">Az.Sql</span></span>
* <span data-ttu-id="11563-369">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="11563-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-370">Az.Storage</span></span>
* <span data-ttu-id="11563-371">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="11563-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="11563-372">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="11563-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="11563-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11563-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="11563-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11563-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="11563-375">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="11563-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="11563-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11563-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-377">Az.Websites</span></span>
* <span data-ttu-id="11563-378">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="11563-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="11563-379">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-380">Az.Accounts</span></span>
* <span data-ttu-id="11563-381">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11563-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="11563-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="11563-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="11563-383">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="11563-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-384">Az.Automation</span></span>
* <span data-ttu-id="11563-385">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="11563-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-387">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="11563-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-388">Az.Compute</span></span>
* <span data-ttu-id="11563-389">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="11563-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11563-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11563-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11563-391">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="11563-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="11563-392">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="11563-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-393">Az.DataFactory</span></span>
* <span data-ttu-id="11563-394">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="11563-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="11563-395">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="11563-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11563-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-396">Az.EventHub</span></span>
* <span data-ttu-id="11563-397">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11563-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11563-398">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="11563-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11563-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-399">Az.KeyVault</span></span>
* <span data-ttu-id="11563-400">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="11563-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11563-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11563-401">Az.LogicApp</span></span>
* <span data-ttu-id="11563-402">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="11563-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="11563-403">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="11563-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="11563-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="11563-404">Az.ManagedServices</span></span>
* <span data-ttu-id="11563-405">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="11563-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-406">Az.Network</span></span>
* <span data-ttu-id="11563-407">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="11563-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="11563-408">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-408">New cmdlets</span></span>
        - <span data-ttu-id="11563-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11563-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11563-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11563-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11563-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11563-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11563-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11563-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11563-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11563-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11563-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="11563-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="11563-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="11563-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="11563-417">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="11563-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="11563-418">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="11563-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="11563-419">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11563-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="11563-420">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="11563-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="11563-421">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="11563-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="11563-422">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="11563-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="11563-423">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="11563-423">Updated cmdlets</span></span>
        - <span data-ttu-id="11563-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11563-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="11563-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="11563-427">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="11563-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="11563-428">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="11563-429">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11563-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="11563-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11563-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="11563-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="11563-433">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="11563-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="11563-434">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="11563-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="11563-435">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="11563-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-437">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="11563-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="11563-438">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="11563-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-440">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11563-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11563-441">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="11563-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="11563-442">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="11563-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="11563-443">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="11563-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="11563-444">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="11563-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="11563-445">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11563-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11563-446">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="11563-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="11563-447">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="11563-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="11563-448">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="11563-449">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="11563-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-450">Az.Resources</span></span>
- <span data-ttu-id="11563-451">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11563-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="11563-452">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="11563-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-453">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-454">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="11563-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="11563-455">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="11563-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-456">Az.Sql</span></span>
* <span data-ttu-id="11563-457">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="11563-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="11563-458">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="11563-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="11563-459">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="11563-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-460">Az.Storage</span></span>
* <span data-ttu-id="11563-461">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="11563-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11563-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11563-462">Az.StorageSync</span></span>
* <span data-ttu-id="11563-463">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="11563-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="11563-464">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="11563-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-465">Az.Websites</span></span>
* <span data-ttu-id="11563-466">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="11563-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="11563-467">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="11563-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="11563-468">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="11563-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="11563-469">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-470">Az.Accounts</span></span>
* <span data-ttu-id="11563-471">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="11563-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="11563-472">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="11563-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="11563-473">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="11563-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="11563-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11563-474">Az.Advisor</span></span>
* <span data-ttu-id="11563-475">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="11563-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="11563-476">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="11563-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="11563-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-477">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-478">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="11563-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="11563-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11563-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="11563-480">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="11563-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="11563-481">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="11563-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="11563-482">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="11563-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="11563-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11563-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="11563-484">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="11563-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-485">Az.Automation</span></span>
* <span data-ttu-id="11563-486">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="11563-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-487">Az.Compute</span></span>
* <span data-ttu-id="11563-488">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="11563-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-489">Az.DataFactory</span></span>
* <span data-ttu-id="11563-490">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="11563-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11563-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11563-491">Az.EventGrid</span></span>
* <span data-ttu-id="11563-492">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="11563-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-493">Az.IotHub</span></span>
* <span data-ttu-id="11563-494">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="11563-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-495">Az.Network</span></span>
* <span data-ttu-id="11563-496">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="11563-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="11563-497">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="11563-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11563-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11563-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="11563-499">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="11563-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="11563-500">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="11563-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-502">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="11563-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-504">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="11563-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-505">Az.Resources</span></span>
    - <span data-ttu-id="11563-506">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="11563-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="11563-507">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="11563-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="11563-508">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="11563-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="11563-509">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="11563-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-510">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-511">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="11563-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-512">Az.Sql</span></span>
* <span data-ttu-id="11563-513">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="11563-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="11563-514">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11563-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="11563-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11563-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11563-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11563-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11563-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="11563-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="11563-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11563-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11563-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11563-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="11563-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="11563-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="11563-521">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="11563-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-522">Az.Storage</span></span>
* <span data-ttu-id="11563-523">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11563-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="11563-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11563-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="11563-525">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="11563-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="11563-526">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="11563-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="11563-527">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="11563-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="11563-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="11563-530">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="11563-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="11563-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11563-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="11563-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="11563-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="11563-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="11563-533">Az.StorageSync</span></span>
* <span data-ttu-id="11563-534">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="11563-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="11563-535">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-536">Az.Accounts</span></span>
* <span data-ttu-id="11563-537">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="11563-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="11563-538">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="11563-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="11563-539">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="11563-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="11563-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11563-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="11563-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="11563-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-542">Az.Compute</span></span>
* <span data-ttu-id="11563-543">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="11563-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="11563-544">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="11563-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="11563-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11563-545">Az.Dns</span></span>
* <span data-ttu-id="11563-546">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="11563-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11563-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11563-547">Az.EventGrid</span></span>
* <span data-ttu-id="11563-548">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="11563-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="11563-549">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="11563-549">New cmdlets:</span></span>
    - <span data-ttu-id="11563-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11563-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11563-551">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11563-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11563-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11563-553">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="11563-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="11563-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="11563-555">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11563-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11563-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11563-557">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="11563-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="11563-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="11563-559">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="11563-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="11563-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="11563-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11563-561">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="11563-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="11563-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="11563-563">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="11563-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="11563-564">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="11563-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="11563-565">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="11563-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="11563-566">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="11563-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="11563-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="11563-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="11563-568">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11563-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11563-569">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11563-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="11563-570">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="11563-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="11563-571">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11563-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="11563-572">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="11563-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="11563-573">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="11563-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="11563-574">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="11563-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="11563-575">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="11563-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="11563-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="11563-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="11563-577">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="11563-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="11563-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="11563-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="11563-579">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11563-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="11563-580">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="11563-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11563-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11563-581">Az.FrontDoor</span></span>
* <span data-ttu-id="11563-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="11563-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="11563-583">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="11563-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="11563-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="11563-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="11563-585">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="11563-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-586">Az.Network</span></span>
* <span data-ttu-id="11563-587">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="11563-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="11563-588">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-588">New cmdlets</span></span>
        - <span data-ttu-id="11563-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="11563-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="11563-590">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11563-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="11563-591">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-591">New cmdlets</span></span>
        - <span data-ttu-id="11563-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="11563-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="11563-593">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="11563-594">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-594">New cmdlets</span></span>
        - <span data-ttu-id="11563-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11563-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11563-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="11563-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="11563-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="11563-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11563-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="11563-600">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11563-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="11563-601">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-601">New cmdlets</span></span>
        - <span data-ttu-id="11563-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11563-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11563-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11563-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11563-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="11563-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="11563-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="11563-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="11563-606">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="11563-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="11563-607">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="11563-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="11563-608">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="11563-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="11563-609">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="11563-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="11563-610">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="11563-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="11563-611">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="11563-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="11563-612">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="11563-613">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="11563-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="11563-614">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="11563-615">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="11563-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="11563-616">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="11563-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="11563-617">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="11563-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="11563-618">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="11563-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="11563-619">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="11563-620">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="11563-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="11563-621">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="11563-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="11563-622">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11563-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="11563-623">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="11563-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="11563-624">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="11563-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="11563-625">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="11563-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="11563-626">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11563-627">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="11563-628">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-630">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="11563-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-631">Az.Resources</span></span>
* <span data-ttu-id="11563-632">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="11563-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="11563-633">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11563-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11563-634">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11563-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="11563-635">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="11563-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-637">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="11563-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-638">Az.Sql</span></span>
* <span data-ttu-id="11563-639">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11563-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="11563-640">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11563-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="11563-641">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="11563-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="11563-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11563-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11563-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11563-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11563-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="11563-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="11563-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11563-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="11563-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11563-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-647">Az.Storage</span></span>
* <span data-ttu-id="11563-648">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11563-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="11563-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="11563-650">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="11563-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="11563-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-652">Az.Websites</span></span>
* <span data-ttu-id="11563-653">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="11563-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="11563-654">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="11563-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="11563-655">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="11563-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11563-656">Az.Cdn</span></span>
* <span data-ttu-id="11563-657">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="11563-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-658">Az.Compute</span></span>
* <span data-ttu-id="11563-659">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="11563-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="11563-660">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="11563-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11563-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-661">Az.EventHub</span></span>
* <span data-ttu-id="11563-662">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="11563-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="11563-663">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11563-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-664">Az.Network</span></span>
* <span data-ttu-id="11563-665">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="11563-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="11563-666">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="11563-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11563-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11563-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="11563-668">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="11563-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-670">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="11563-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-671">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-672">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11563-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-674">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="11563-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="11563-675">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="11563-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-676">Az.Sql</span></span>
* <span data-ttu-id="11563-677">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="11563-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="11563-678">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="11563-679">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="11563-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="11563-680">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="11563-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-681">Az.Websites</span></span>
* <span data-ttu-id="11563-682">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="11563-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="11563-683">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="11563-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-684">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-685">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="11563-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="11563-686">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11563-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="11563-687">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11563-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="11563-688">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="11563-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="11563-689">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="11563-690">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="11563-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="11563-691">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11563-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="11563-692">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="11563-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="11563-693">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="11563-694">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="11563-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="11563-695">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="11563-696">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="11563-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="11563-697">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="11563-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="11563-698">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="11563-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="11563-699">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="11563-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="11563-700">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="11563-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="11563-701">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="11563-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="11563-702">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="11563-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="11563-703">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="11563-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="11563-704">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="11563-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="11563-705">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="11563-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="11563-706">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="11563-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="11563-707">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="11563-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="11563-708">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="11563-709">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="11563-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="11563-710">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="11563-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="11563-711">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="11563-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="11563-712">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="11563-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="11563-713">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="11563-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="11563-714">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="11563-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="11563-715">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="11563-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="11563-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="11563-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="11563-717">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="11563-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="11563-718">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11563-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11563-719">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="11563-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="11563-720">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="11563-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="11563-721">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="11563-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="11563-722">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="11563-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="11563-723">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="11563-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="11563-724">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11563-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11563-725">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="11563-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11563-726">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11563-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="11563-727">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="11563-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="11563-728">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="11563-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="11563-729">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="11563-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="11563-730">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="11563-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="11563-731">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11563-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="11563-732">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="11563-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="11563-733">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="11563-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="11563-734">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="11563-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="11563-735">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="11563-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="11563-736">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="11563-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="11563-737">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="11563-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="11563-738">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="11563-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="11563-739">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="11563-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="11563-740">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="11563-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="11563-741">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11563-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11563-742">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11563-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11563-743">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11563-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11563-744">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="11563-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11563-745">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="11563-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="11563-746">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11563-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="11563-747">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="11563-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="11563-748">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="11563-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="11563-749">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="11563-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="11563-750">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="11563-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="11563-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="11563-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="11563-752">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="11563-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="11563-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="11563-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="11563-754">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11563-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="11563-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="11563-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="11563-756">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="11563-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="11563-757">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="11563-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="11563-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="11563-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="11563-759">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="11563-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="11563-760">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="11563-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="11563-761">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="11563-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-762">Az.Automation</span></span>
* <span data-ttu-id="11563-763">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="11563-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="11563-764">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="11563-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="11563-765">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="11563-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="11563-766">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="11563-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="11563-767">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="11563-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="11563-768">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="11563-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="11563-769">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="11563-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-770">Az.Compute</span></span>
* <span data-ttu-id="11563-771">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="11563-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="11563-772">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="11563-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-774">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-775">Az.Monitor</span></span>
* <span data-ttu-id="11563-776">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-777">Az.Network</span></span>
* <span data-ttu-id="11563-778">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="11563-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="11563-779">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="11563-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="11563-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="11563-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="11563-781">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11563-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-782">Az.Resources</span></span>
* <span data-ttu-id="11563-783">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="11563-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-784">Az.Sql</span></span>
* <span data-ttu-id="11563-785">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="11563-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="11563-786">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-787">Az.Accounts</span></span>
* <span data-ttu-id="11563-788">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="11563-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-790">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="11563-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="11563-791">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="11563-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-792">Az.Compute</span></span>
* <span data-ttu-id="11563-793">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="11563-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="11563-794">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="11563-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="11563-795">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11563-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="11563-796">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="11563-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="11563-797">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="11563-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="11563-798">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11563-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="11563-799">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="11563-799">Breaking changes</span></span>
    - <span data-ttu-id="11563-800">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="11563-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="11563-801">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="11563-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="11563-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="11563-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="11563-803">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="11563-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="11563-804">Az.Dns</span></span>
* <span data-ttu-id="11563-805">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="11563-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="11563-806">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="11563-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="11563-807">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="11563-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="11563-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11563-808">Az.FrontDoor</span></span>
* <span data-ttu-id="11563-809">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="11563-810">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="11563-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="11563-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11563-811">Az.HDInsight</span></span>
* <span data-ttu-id="11563-812">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="11563-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="11563-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11563-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="11563-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11563-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11563-815">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="11563-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="11563-816">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="11563-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="11563-817">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="11563-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="11563-818">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="11563-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-819">Az.Monitor</span></span>
* <span data-ttu-id="11563-820">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="11563-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="11563-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="11563-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="11563-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="11563-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="11563-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="11563-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="11563-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="11563-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="11563-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="11563-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="11563-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="11563-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="11563-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11563-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11563-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11563-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11563-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11563-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11563-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11563-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11563-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="11563-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="11563-832">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="11563-832">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="11563-833">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="11563-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-834">Az.Network</span></span>
* <span data-ttu-id="11563-835">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="11563-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="11563-836">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="11563-836">New cmdlets</span></span>
        - <span data-ttu-id="11563-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11563-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="11563-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11563-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="11563-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11563-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="11563-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="11563-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="11563-841">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="11563-841">Updated cmdlets</span></span>
        - <span data-ttu-id="11563-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11563-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="11563-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="11563-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="11563-844">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="11563-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="11563-845">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="11563-846">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="11563-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11563-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11563-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="11563-848">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="11563-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="11563-849">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="11563-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="11563-850">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="11563-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-852">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11563-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="11563-853">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11563-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="11563-854">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11563-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="11563-855">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="11563-856">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11563-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="11563-857">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="11563-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="11563-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11563-858">Az.Relay</span></span>
* <span data-ttu-id="11563-859">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="11563-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-860">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-861">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="11563-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-862">Az.Storage</span></span>
* <span data-ttu-id="11563-863">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="11563-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="11563-864">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="11563-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="11563-865">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="11563-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="11563-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="11563-867">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="11563-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="11563-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="11563-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="11563-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-871">Az.Websites</span></span>
* <span data-ttu-id="11563-872">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="11563-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="11563-873">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="11563-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="11563-874">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11563-875">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11563-875">Highlights since the last major release</span></span>
* <span data-ttu-id="11563-876">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11563-876">General availability of `Az` module</span></span>
* <span data-ttu-id="11563-877">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11563-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11563-878">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11563-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11563-879">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11563-880">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11563-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11563-881">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11563-882">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11563-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11563-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-883">Az.Accounts</span></span>
* <span data-ttu-id="11563-884">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="11563-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="11563-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11563-885">Az.Batch</span></span>
* <span data-ttu-id="11563-886">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11563-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11563-887">Az.Cdn</span></span>
* <span data-ttu-id="11563-888">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-890">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-891">Az.Compute</span></span>
* <span data-ttu-id="11563-892">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="11563-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="11563-893">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-894">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11563-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-895">Az.DataFactory</span></span>
* <span data-ttu-id="11563-896">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11563-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-898">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11563-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11563-899">Az.EventGrid</span></span>
* <span data-ttu-id="11563-900">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="11563-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11563-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-901">Az.EventHub</span></span>
* <span data-ttu-id="11563-902">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="11563-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="11563-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="11563-903">Az.HDInsight</span></span>
* <span data-ttu-id="11563-904">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-905">Az.IotHub</span></span>
* <span data-ttu-id="11563-906">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11563-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-907">Az.KeyVault</span></span>
* <span data-ttu-id="11563-908">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-909">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11563-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="11563-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11563-910">Az.MachineLearning</span></span>
* <span data-ttu-id="11563-911">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="11563-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11563-912">Az.Media</span></span>
* <span data-ttu-id="11563-913">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-914">Az.Monitor</span></span>
  * <span data-ttu-id="11563-915">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="11563-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="11563-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="11563-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="11563-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="11563-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="11563-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11563-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11563-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11563-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="11563-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="11563-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="11563-921">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="11563-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-922">Az.Network</span></span>
* <span data-ttu-id="11563-923">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-924">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11563-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="11563-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="11563-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="11563-926">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-928">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="11563-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="11563-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="11563-930">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-932">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-933">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="11563-934">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="11563-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="11563-935">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="11563-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11563-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11563-936">Az.RedisCache</span></span>
* <span data-ttu-id="11563-937">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-938">Az.Resources</span></span>
* <span data-ttu-id="11563-939">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11563-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-940">Az.Sql</span></span>
* <span data-ttu-id="11563-941">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="11563-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="11563-942">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-943">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="11563-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="11563-944">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="11563-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="11563-945">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="11563-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="11563-946">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="11563-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="11563-947">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="11563-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-948">Az.Websites</span></span>
* <span data-ttu-id="11563-949">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="11563-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="11563-950">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="11563-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="11563-951">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="11563-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="11563-952">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="11563-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="11563-953">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11563-954">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11563-954">Highlights since the last major release</span></span>
* <span data-ttu-id="11563-955">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11563-955">General availability of `Az` module</span></span>
* <span data-ttu-id="11563-956">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11563-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11563-957">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11563-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11563-958">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11563-959">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11563-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11563-960">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11563-961">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11563-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="11563-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-962">Az.Accounts</span></span>
* <span data-ttu-id="11563-963">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="11563-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11563-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11563-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="11563-965">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="11563-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="11563-966">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="11563-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-967">Az.Automation</span></span>
* <span data-ttu-id="11563-968">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="11563-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="11563-969">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="11563-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="11563-970">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-971">Az.Compute</span></span>
* <span data-ttu-id="11563-972">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="11563-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="11563-973">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="11563-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="11563-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11563-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="11563-975">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="11563-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-976">Az.DataFactory</span></span>
* <span data-ttu-id="11563-977">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="11563-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="11563-978">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11563-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-979">Az.Resources</span></span>
* <span data-ttu-id="11563-980">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="11563-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="11563-981">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11563-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="11563-982">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="11563-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="11563-983">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11563-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="11563-984">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="11563-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="11563-985">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="11563-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-986">Az.Sql</span></span>
* <span data-ttu-id="11563-987">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="11563-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-988">Az.Storage</span></span>
* <span data-ttu-id="11563-989">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="11563-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11563-990">New-AzStorageContext</span></span>
* <span data-ttu-id="11563-991">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="11563-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="11563-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11563-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11563-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="11563-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="11563-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="11563-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="11563-996">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="11563-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="11563-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11563-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11563-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="11563-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="11563-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11563-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="11563-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="11563-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="11563-1001">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="11563-1002">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="11563-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="11563-1003">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="11563-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="11563-1004">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="11563-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="11563-1005">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="11563-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="11563-1006">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="11563-1007">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11563-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11563-1008">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="11563-1009">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="11563-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1010">Az.Automation</span></span>
* <span data-ttu-id="11563-1011">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="11563-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="11563-1012">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="11563-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="11563-1013">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="11563-1013">Pre-Post script</span></span>
    * <span data-ttu-id="11563-1014">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="11563-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1015">Az.Compute</span></span>
* <span data-ttu-id="11563-1016">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="11563-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="11563-1017">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="11563-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11563-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-1018">Az.KeyVault</span></span>
* <span data-ttu-id="11563-1019">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1020">Az.Network</span></span>
* <span data-ttu-id="11563-1021">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="11563-1022">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="11563-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-1024">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="11563-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="11563-1025">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="11563-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1026">Az.Resources</span></span>
* <span data-ttu-id="11563-1027">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11563-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="11563-1028">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="11563-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1029">Az.Sql</span></span>
* <span data-ttu-id="11563-1030">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="11563-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1031">Az.Storage</span></span>
* <span data-ttu-id="11563-1032">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="11563-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="11563-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11563-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11563-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="11563-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="11563-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="11563-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="11563-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="11563-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="11563-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1039">Az.Websites</span></span>
* <span data-ttu-id="11563-1040">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="11563-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="11563-1041">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1042">Az.Accounts</span></span>
* <span data-ttu-id="11563-1043">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="11563-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="11563-1044">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1045">Az.Automation</span></span>
* <span data-ttu-id="11563-1046">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="11563-1047">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="11563-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="11563-1048">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="11563-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11563-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11563-1049">Az.Cdn</span></span>
* <span data-ttu-id="11563-1050">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="11563-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1051">Az.Compute</span></span>
* <span data-ttu-id="11563-1052">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="11563-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-1053">Az.DataFactory</span></span>
* <span data-ttu-id="11563-1054">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="11563-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11563-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11563-1055">Az.LogicApp</span></span>
* <span data-ttu-id="11563-1056">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="11563-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1057">Az.Network</span></span>
* <span data-ttu-id="11563-1058">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="11563-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-1060">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="11563-1061">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="11563-1061">SDK Update</span></span>
* <span data-ttu-id="11563-1062">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11563-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="11563-1063">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11563-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1064">Az.Resources</span></span>
* <span data-ttu-id="11563-1065">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="11563-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="11563-1066">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="11563-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="11563-1067">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="11563-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="11563-1068">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="11563-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="11563-1069">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="11563-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="11563-1070">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="11563-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1071">Az.Sql</span></span>
* <span data-ttu-id="11563-1072">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="11563-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="11563-1073">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="11563-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1074">Az.Storage</span></span>
* <span data-ttu-id="11563-1075">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="11563-1076">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="11563-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11563-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="11563-1078">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1079">Az.Automation</span></span>
* <span data-ttu-id="11563-1080">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="11563-1081">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="11563-1082">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-1084">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="11563-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1085">Az.Compute</span></span>
* <span data-ttu-id="11563-1086">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="11563-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="11563-1087">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="11563-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="11563-1088">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="11563-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="11563-1089">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="11563-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-1091">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="11563-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="11563-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-1092">Az.EventHub</span></span>
* <span data-ttu-id="11563-1093">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="11563-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11563-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-1094">Az.KeyVault</span></span>
* <span data-ttu-id="11563-1095">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11563-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11563-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11563-1096">Az.LogicApp</span></span>
* <span data-ttu-id="11563-1097">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="11563-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="11563-1098">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="11563-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="11563-1099">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="11563-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="11563-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11563-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11563-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11563-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11563-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11563-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="11563-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="11563-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="11563-1104">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="11563-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="11563-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11563-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11563-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="11563-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="11563-1109">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="11563-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="11563-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-1110">Az.Monitor</span></span>
* <span data-ttu-id="11563-1111">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="11563-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1112">Az.Network</span></span>
* <span data-ttu-id="11563-1113">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="11563-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="11563-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="11563-1115">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="11563-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="11563-1116">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="11563-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="11563-1117">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="11563-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1118">Az.Resources</span></span>
* <span data-ttu-id="11563-1119">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="11563-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11563-1120">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="11563-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="11563-1121">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="11563-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="11563-1122">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="11563-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1123">Az.Sql</span></span>
* <span data-ttu-id="11563-1124">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="11563-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="11563-1125">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="11563-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1126">Az.Websites</span></span>
* <span data-ttu-id="11563-1127">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="11563-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="11563-1128">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1129">Az.Accounts</span></span>
* <span data-ttu-id="11563-1130">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11563-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11563-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11563-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="11563-1132">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="11563-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1133">Az.Compute</span></span>
* <span data-ttu-id="11563-1134">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="11563-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="11563-1135">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="11563-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="11563-1136">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="11563-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="11563-1138">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="11563-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1139">Az.Resources</span></span>
* <span data-ttu-id="11563-1140">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="11563-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="11563-1141">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="11563-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="11563-1142">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="11563-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="11563-1143">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="11563-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1144">Az.Sql</span></span>
* <span data-ttu-id="11563-1145">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="11563-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="11563-1146">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="11563-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="11563-1147">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="11563-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="11563-1148">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1149">Az.Accounts</span></span>
* <span data-ttu-id="11563-1150">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="11563-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="11563-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="11563-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="11563-1152">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="11563-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="11563-1154">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="11563-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="11563-1155">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1156">Az.Accounts</span></span>
* <span data-ttu-id="11563-1157">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="11563-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="11563-1158">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11563-1159">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="11563-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="11563-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="11563-1160">Az.Aks</span></span>
* <span data-ttu-id="11563-1161">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="11563-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1162">Az.Automation</span></span>
* <span data-ttu-id="11563-1163">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="11563-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="11563-1164">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="11563-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="11563-1165">Az.Cdn</span></span>
* <span data-ttu-id="11563-1166">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1167">Az.Compute</span></span>
* <span data-ttu-id="11563-1168">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="11563-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="11563-1169">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="11563-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="11563-1170">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="11563-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="11563-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="11563-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="11563-1172">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="11563-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="11563-1173">Az.DataFactory</span></span>
* <span data-ttu-id="11563-1174">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="11563-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-1176">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="11563-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="11563-1177">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="11563-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="11563-1178">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-1179">Az.IotHub</span></span>
* <span data-ttu-id="11563-1180">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="11563-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="11563-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-1181">Az.KeyVault</span></span>
* <span data-ttu-id="11563-1182">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1183">Az.Network</span></span>
* <span data-ttu-id="11563-1184">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1185">Az.Resources</span></span>
* <span data-ttu-id="11563-1186">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="11563-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="11563-1187">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="11563-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="11563-1188">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="11563-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="11563-1189">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="11563-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="11563-1190">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="11563-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="11563-1191">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="11563-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="11563-1192">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="11563-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-1194">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="11563-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="11563-1195">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="11563-1195">Fix some error messages.</span></span>
* <span data-ttu-id="11563-1196">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="11563-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="11563-1197">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="11563-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11563-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11563-1198">Az.SignalR</span></span>
* <span data-ttu-id="11563-1199">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1200">Az.Sql</span></span>
* <span data-ttu-id="11563-1201">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11563-1202">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="11563-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="11563-1203">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="11563-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="11563-1204">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="11563-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1205">Az.Storage</span></span>
* <span data-ttu-id="11563-1206">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11563-1207">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="11563-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="11563-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="11563-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="11563-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="11563-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="11563-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="11563-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="11563-1211">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1212">Az.Websites</span></span>
* <span data-ttu-id="11563-1213">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="11563-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="11563-1214">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="11563-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="11563-1215">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="11563-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="11563-1216">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="11563-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="11563-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1217">Az.Accounts</span></span>
* <span data-ttu-id="11563-1218">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="11563-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1219">Az.Compute</span></span>
* <span data-ttu-id="11563-1220">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="11563-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="11563-1221">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="11563-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="11563-1222">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-1224">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="11563-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="11563-1225">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="11563-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="11563-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="11563-1226">Az.EventGrid</span></span>
* <span data-ttu-id="11563-1227">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="11563-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="11563-1228">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="11563-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="11563-1229">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11563-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11563-1230">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="11563-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11563-1231">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="11563-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11563-1232">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="11563-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="11563-1233">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="11563-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="11563-1234">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="11563-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="11563-1235">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="11563-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="11563-1236">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="11563-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="11563-1237">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="11563-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="11563-1238">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="11563-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="11563-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-1239">Az.IotHub</span></span>
* <span data-ttu-id="11563-1240">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="11563-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="11563-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="11563-1241">Az.LogicApp</span></span>
* <span data-ttu-id="11563-1242">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="11563-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1243">Az.Resources</span></span>
* <span data-ttu-id="11563-1244">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="11563-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="11563-1245">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="11563-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="11563-1246">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11563-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11563-1247">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="11563-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="11563-1248">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="11563-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="11563-1249">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="11563-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="11563-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="11563-1250">Az.SignalR</span></span>
* <span data-ttu-id="11563-1251">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1252">Az.Sql</span></span>
* <span data-ttu-id="11563-1253">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="11563-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="11563-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1254">Az.Storage</span></span>
* <span data-ttu-id="11563-1255">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="11563-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="11563-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11563-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="11563-1257">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="11563-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="11563-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="11563-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1259">Az.Websites</span></span>
* <span data-ttu-id="11563-1260">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="11563-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="11563-1261">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="11563-1262">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="11563-1263">Geral</span><span class="sxs-lookup"><span data-stu-id="11563-1263">General</span></span>

- <span data-ttu-id="11563-1264">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="11563-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="11563-1265">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="11563-1265">Online help for each module</span></span>
- <span data-ttu-id="11563-1266">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="11563-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="11563-1267">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="11563-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="11563-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1268">Az.Accounts</span></span>
- <span data-ttu-id="11563-1269">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11563-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="11563-1270">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="11563-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11563-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="11563-1272">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="11563-1272">Fixes for #7002</span></span>
- <span data-ttu-id="11563-1273">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="11563-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="11563-1274">Az.Batch</span></span>
- <span data-ttu-id="11563-1275">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="11563-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="11563-1276">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="11563-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="11563-1277">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="11563-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="11563-1278">Az.Billing</span></span>
- <span data-ttu-id="11563-1279">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="11563-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="11563-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="11563-1281">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="11563-1282">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="11563-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11563-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="11563-1284">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="11563-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="11563-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="11563-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="11563-1286">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11563-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="11563-1288">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="11563-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="11563-1289">Az.Monitor</span></span>
- <span data-ttu-id="11563-1290">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="11563-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="11563-1291">Az.KeyVault</span></span>
- <span data-ttu-id="11563-1292">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="11563-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="11563-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="11563-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="11563-1294">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="11563-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="11563-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="11563-1295">Az.Media</span></span>
- <span data-ttu-id="11563-1296">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11563-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11563-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1297">Az.Network</span></span>
<span data-ttu-id="11563-1298">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="11563-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="11563-1299">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="11563-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="11563-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="11563-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="11563-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="11563-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="11563-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="11563-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="11563-1308">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="11563-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="11563-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11563-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="11563-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11563-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11563-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="11563-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="11563-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11563-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="11563-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11563-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="11563-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="11563-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="11563-1315">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11563-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="11563-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11563-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11563-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11563-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="11563-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="11563-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="11563-1319">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="11563-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="11563-1320">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="11563-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="11563-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="11563-1322">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="11563-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11563-1323">Az.Profile</span></span>
- <span data-ttu-id="11563-1324">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="11563-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="11563-1326">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="11563-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1327">Az.Resources</span></span>
- <span data-ttu-id="11563-1328">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11563-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="11563-1330">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="11563-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="11563-1331">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="11563-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="11563-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="11563-1333">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="11563-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="11563-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1334">Az.Sql</span></span>
- <span data-ttu-id="11563-1335">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="11563-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="11563-1336">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="11563-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="11563-1337">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="11563-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1338">Az.Storage</span></span>
- <span data-ttu-id="11563-1339">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11563-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1340">Az.Websites</span></span>
- <span data-ttu-id="11563-1341">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="11563-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="11563-1342">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="11563-1343">Geral</span><span class="sxs-lookup"><span data-stu-id="11563-1343">General</span></span>

* <span data-ttu-id="11563-1344">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="11563-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="11563-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1345">Az.Compute</span></span>

* <span data-ttu-id="11563-1346">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="11563-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="11563-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="11563-1348">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="11563-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="11563-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="11563-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="11563-1350">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="11563-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="11563-1351">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="11563-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="11563-1352">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="11563-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="11563-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="11563-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="11563-1354">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="11563-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="11563-1355">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="11563-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="11563-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1356">Az.Resources</span></span>

* <span data-ttu-id="11563-1357">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="11563-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="11563-1358">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="11563-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="11563-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1359">Az.Sql</span></span>

* <span data-ttu-id="11563-1360">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="11563-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="11563-1361">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="11563-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="11563-1362">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="11563-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="11563-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1363">Az.Storage</span></span>

* <span data-ttu-id="11563-1364">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="11563-1365">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="11563-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="11563-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11563-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11563-1367">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="11563-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="11563-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11563-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="11563-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="11563-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="11563-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1370">Az.Websites</span></span>

* <span data-ttu-id="11563-1371">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="11563-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="11563-1372">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="11563-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="11563-1373">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="11563-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="11563-1374">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="11563-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="11563-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="11563-1376">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11563-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="11563-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="11563-1377">Az.Automation</span></span>
* <span data-ttu-id="11563-1378">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="11563-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="11563-1379">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="11563-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="11563-1380">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="11563-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="11563-1381">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="11563-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="11563-1382">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="11563-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="11563-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1383">Az.Compute</span></span>
* <span data-ttu-id="11563-1384">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="11563-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="11563-1385">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11563-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="11563-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="11563-1387">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11563-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="11563-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="11563-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="11563-1389">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="11563-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="11563-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1390">Az.Network</span></span>
* <span data-ttu-id="11563-1391">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="11563-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="11563-1392">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="11563-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="11563-1393">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="11563-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="11563-1394">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="11563-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="11563-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="11563-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="11563-1396">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="11563-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="11563-1397">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="11563-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="11563-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="11563-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="11563-1399">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="11563-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="11563-1400">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="11563-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="11563-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="11563-1401">Az.Relay</span></span>
* <span data-ttu-id="11563-1402">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="11563-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="11563-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1403">Az.Resources</span></span>
* <span data-ttu-id="11563-1404">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="11563-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="11563-1405">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="11563-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="11563-1406">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="11563-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="11563-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-1408">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="11563-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="11563-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1409">Az.Sql</span></span>
* <span data-ttu-id="11563-1410">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="11563-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="11563-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11563-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11563-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11563-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="11563-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="11563-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11563-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11563-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11563-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11563-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11563-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="11563-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="11563-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="11563-1419">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="11563-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="11563-1420">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="11563-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="11563-1421">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="11563-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="11563-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="11563-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11563-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="11563-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="11563-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="11563-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="11563-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="11563-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="11563-1426">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="11563-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="11563-1427">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="11563-1428">Geral</span><span class="sxs-lookup"><span data-stu-id="11563-1428">General</span></span>
* <span data-ttu-id="11563-1429">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="11563-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="11563-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11563-1430">Az.Profile</span></span>
* <span data-ttu-id="11563-1431">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11563-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="11563-1432">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="11563-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="11563-1433">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="11563-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="11563-1434">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="11563-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="11563-1435">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="11563-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="11563-1436">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="11563-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="11563-1437">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="11563-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-1439">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="11563-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1440">Az.Compute</span></span>
* <span data-ttu-id="11563-1441">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="11563-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="11563-1442">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="11563-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="11563-1443">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="11563-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-1445">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="11563-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="11563-1446">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="11563-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="11563-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="11563-1447">Az.Insights</span></span>
* <span data-ttu-id="11563-1448">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="11563-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="11563-1449">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="11563-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="11563-1450">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="11563-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="11563-1451">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="11563-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1452">Az.Network</span></span>
* <span data-ttu-id="11563-1453">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="11563-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="11563-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="11563-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="11563-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="11563-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="11563-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11563-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="11563-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="11563-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="11563-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="11563-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="11563-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="11563-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="11563-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="11563-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="11563-1461">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="11563-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1462">Az.Resources</span></span>
* <span data-ttu-id="11563-1463">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="11563-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="11563-1464">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="11563-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="11563-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="11563-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="11563-1466">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="11563-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="11563-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="11563-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="11563-1468">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="11563-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="11563-1469">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="11563-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="11563-1470">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="11563-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="11563-1471">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="11563-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="11563-1472">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="11563-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="11563-1473">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="11563-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="11563-1474">Az.Profile</span></span>
* <span data-ttu-id="11563-1475">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="11563-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="11563-1476">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="11563-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1477">Az.Compute</span></span>
* <span data-ttu-id="11563-1478">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="11563-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="11563-1479">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11563-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="11563-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="11563-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="11563-1481">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="11563-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="11563-1482">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11563-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="11563-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="11563-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11563-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="11563-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="11563-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11563-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1486">Az.Network</span></span>
* <span data-ttu-id="11563-1487">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="11563-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="11563-1488">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="11563-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1489">Az.Resources</span></span>
* <span data-ttu-id="11563-1490">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="11563-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="11563-1491">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="11563-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="11563-1492">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="11563-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="11563-1493">Azure.Storage</span></span>
* <span data-ttu-id="11563-1494">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="11563-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="11563-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="11563-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="11563-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11563-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="11563-1497">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="11563-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="11563-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="11563-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="11563-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="11563-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="11563-1500">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="11563-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="11563-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="11563-1501">Az.Compute</span></span>
* <span data-ttu-id="11563-1502">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="11563-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="11563-1503">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="11563-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="11563-1504">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="11563-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="11563-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="11563-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="11563-1506">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="11563-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="11563-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="11563-1507">Az.Network</span></span>
* <span data-ttu-id="11563-1508">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="11563-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="11563-1509">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="11563-1509">new cmdlets added</span></span>
    - <span data-ttu-id="11563-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11563-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="11563-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11563-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="11563-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11563-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="11563-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="11563-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="11563-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="11563-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="11563-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="11563-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="11563-1516">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="11563-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="11563-1517">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="11563-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="11563-1518">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="11563-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="11563-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="11563-1519">Az.RedisCache</span></span>
* <span data-ttu-id="11563-1520">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="11563-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="11563-1521">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="11563-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="11563-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="11563-1522">Az.Resources</span></span>
* <span data-ttu-id="11563-1523">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11563-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="11563-1524">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="11563-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="11563-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="11563-1525">Az.Sql</span></span>
* <span data-ttu-id="11563-1526">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="11563-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="11563-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="11563-1527">Az.Websites</span></span>
* <span data-ttu-id="11563-1528">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="11563-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="11563-1529">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="11563-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="11563-1530">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="11563-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="11563-1531">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="11563-1531">Initial Release</span></span>
