---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/14/2020
ms.locfileid: "86381756"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="4359b-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4359b-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="4359b-104">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-105">Az.Accounts</span></span>
* <span data-ttu-id="4359b-106">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="4359b-107">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="4359b-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4359b-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4359b-108">Az.Aks</span></span>
* <span data-ttu-id="4359b-109">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="4359b-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="4359b-111">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4359b-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-112">Az.Automation</span></span>
* <span data-ttu-id="4359b-113">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="4359b-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-114">Az.Compute</span></span>
* <span data-ttu-id="4359b-115">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="4359b-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-116">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-117">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4359b-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4359b-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4359b-118">Az.EventGrid</span></span>
* <span data-ttu-id="4359b-119">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="4359b-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="4359b-120">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-120">Added new features:</span></span>
    - <span data-ttu-id="4359b-121">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="4359b-121">Input mapping</span></span>
    - <span data-ttu-id="4359b-122">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="4359b-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="4359b-123">Link Privado</span><span class="sxs-lookup"><span data-stu-id="4359b-123">Private Link</span></span>
    - <span data-ttu-id="4359b-124">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="4359b-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="4359b-125">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="4359b-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="4359b-126">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="4359b-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="4359b-127">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="4359b-127">WebHook Batching</span></span>
    - <span data-ttu-id="4359b-128">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="4359b-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="4359b-129">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="4359b-129">IpFiltering</span></span>
* <span data-ttu-id="4359b-130">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4359b-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="4359b-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="4359b-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="4359b-132">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="4359b-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="4359b-133">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="4359b-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="4359b-134">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="4359b-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="4359b-135">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="4359b-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="4359b-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4359b-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4359b-137">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="4359b-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="4359b-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4359b-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4359b-139">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4359b-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-140">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-141">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="4359b-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="4359b-142">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="4359b-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-143">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-144">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="4359b-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-145">Az.Monitor</span></span>
* <span data-ttu-id="4359b-146">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="4359b-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-147">Az.Network</span></span>
* <span data-ttu-id="4359b-148">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="4359b-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="4359b-149">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="4359b-150">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4359b-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4359b-151">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4359b-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4359b-152">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4359b-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4359b-153">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4359b-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4359b-154">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="4359b-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="4359b-155">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="4359b-156">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4359b-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4359b-157">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4359b-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4359b-158">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4359b-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4359b-159">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4359b-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4359b-160">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="4359b-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="4359b-161">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="4359b-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="4359b-162">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4359b-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4359b-163">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4359b-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4359b-164">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4359b-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-166">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4359b-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="4359b-167">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="4359b-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="4359b-168">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="4359b-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-169">Az.Resources</span></span>
* <span data-ttu-id="4359b-170">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="4359b-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="4359b-171">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-172">Az.Sql</span></span>
* <span data-ttu-id="4359b-173">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="4359b-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="4359b-174">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="4359b-175">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="4359b-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-176">Az.Storage</span></span>
* <span data-ttu-id="4359b-177">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="4359b-178">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="4359b-179">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4359b-180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-181">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4359b-182">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4359b-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4359b-183">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="4359b-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="4359b-184">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4359b-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="4359b-185">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="4359b-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="4359b-186">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4359b-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="4359b-187">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4359b-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="4359b-188">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="4359b-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="4359b-189">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4359b-190">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="4359b-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="4359b-191">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4359b-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="4359b-192">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4359b-193">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="4359b-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4359b-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4359b-194">Az.StorageSync</span></span>
* <span data-ttu-id="4359b-195">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="4359b-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="4359b-196">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="4359b-197">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="4359b-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="4359b-198">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4359b-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-199">Az.Websites</span></span>
* <span data-ttu-id="4359b-200">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="4359b-201">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-202">Az.Accounts</span></span>
* <span data-ttu-id="4359b-203">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="4359b-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="4359b-204">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="4359b-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="4359b-205">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4359b-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="4359b-206">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="4359b-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4359b-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4359b-207">Az.Aks</span></span>
* <span data-ttu-id="4359b-208">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="4359b-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-209">Az.Batch</span></span>
* <span data-ttu-id="4359b-210">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="4359b-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="4359b-211">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-213">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="4359b-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="4359b-214">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4359b-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-215">Az.Compute</span></span>
* <span data-ttu-id="4359b-216">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4359b-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="4359b-217">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4359b-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="4359b-218">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="4359b-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="4359b-219">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4359b-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="4359b-220">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="4359b-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-221">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-222">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="4359b-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-223">Az.EventHub</span></span>
* <span data-ttu-id="4359b-224">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="4359b-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4359b-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4359b-225">Az.Functions</span></span>
* <span data-ttu-id="4359b-226">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="4359b-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-227">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-228">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4359b-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4359b-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4359b-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="4359b-230">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="4359b-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="4359b-231">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4359b-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-232">Az.Monitor</span></span>
* <span data-ttu-id="4359b-233">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="4359b-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="4359b-234">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="4359b-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-235">Az.Network</span></span>
* <span data-ttu-id="4359b-236">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4359b-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4359b-237">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4359b-238">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="4359b-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="4359b-239">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4359b-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="4359b-240">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="4359b-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="4359b-241">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="4359b-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="4359b-242">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4359b-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4359b-243">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4359b-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4359b-244">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4359b-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4359b-245">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4359b-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="4359b-246">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="4359b-247">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4359b-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="4359b-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="4359b-249">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="4359b-250">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4359b-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="4359b-251">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4359b-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="4359b-252">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4359b-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="4359b-253">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="4359b-254">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="4359b-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="4359b-255">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="4359b-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="4359b-256">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4359b-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="4359b-257">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="4359b-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="4359b-258">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4359b-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="4359b-259">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="4359b-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="4359b-260">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4359b-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4359b-261">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4359b-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4359b-262">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="4359b-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="4359b-263">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="4359b-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4359b-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4359b-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4359b-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4359b-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4359b-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="4359b-270">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4359b-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="4359b-271">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="4359b-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="4359b-272">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4359b-273">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4359b-274">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4359b-275">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="4359b-276">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4359b-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="4359b-277">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4359b-278">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4359b-279">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4359b-280">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4359b-281">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="4359b-282">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="4359b-283">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="4359b-284">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-286">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="4359b-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="4359b-287">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4359b-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="4359b-288">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="4359b-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="4359b-289">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4359b-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4359b-290">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4359b-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-292">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="4359b-293">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="4359b-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-294">Az.Resources</span></span>
* <span data-ttu-id="4359b-295">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="4359b-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="4359b-296">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="4359b-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="4359b-297">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4359b-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="4359b-298">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="4359b-299">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="4359b-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="4359b-300">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="4359b-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-301">Az.Sql</span></span>
* <span data-ttu-id="4359b-302">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4359b-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="4359b-303">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="4359b-304">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="4359b-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-305">Az.Storage</span></span>
* <span data-ttu-id="4359b-306">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="4359b-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="4359b-307">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-308">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-309">Az.Websites</span></span>
* <span data-ttu-id="4359b-310">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4359b-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4359b-311">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4359b-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="4359b-312">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4359b-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="4359b-313">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4359b-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="4359b-314">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="4359b-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="4359b-315">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4359b-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="4359b-316">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-317">Az.Accounts</span></span>
* <span data-ttu-id="4359b-318">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="4359b-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="4359b-320">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-321">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-322">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="4359b-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4359b-323">Az.Billing</span></span>
* <span data-ttu-id="4359b-324">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-326">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4359b-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-327">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-328">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="4359b-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="4359b-329">Az.DataShare</span></span>
* <span data-ttu-id="4359b-330">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="4359b-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4359b-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4359b-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4359b-332">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="4359b-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-334">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="4359b-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="4359b-335">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="4359b-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="4359b-336">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4359b-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4359b-337">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4359b-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-339">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="4359b-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4359b-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4359b-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4359b-341">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4359b-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4359b-342">Az.PrivateDns</span></span>
* <span data-ttu-id="4359b-343">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4359b-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-345">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="4359b-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="4359b-346">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4359b-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-347">Az.Resources</span></span>
* <span data-ttu-id="4359b-348">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="4359b-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="4359b-349">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4359b-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="4359b-350">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="4359b-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="4359b-351">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4359b-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="4359b-352">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-353">Az.Sql</span></span>
* <span data-ttu-id="4359b-354">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4359b-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4359b-355">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4359b-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4359b-356">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4359b-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-357">Az.Storage</span></span>
* <span data-ttu-id="4359b-358">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="4359b-359">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4359b-360">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4359b-360">Highlights since the last release</span></span>
* <span data-ttu-id="4359b-361">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4359b-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="4359b-362">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4359b-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="4359b-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-364">Az.Accounts</span></span>
* <span data-ttu-id="4359b-365">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="4359b-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="4359b-366">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="4359b-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="4359b-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4359b-367">Az.Aks</span></span>
* <span data-ttu-id="4359b-368">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4359b-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="4359b-369">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4359b-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="4359b-370">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="4359b-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-371">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-372">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="4359b-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="4359b-373">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="4359b-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="4359b-374">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4359b-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4359b-375">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4359b-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4359b-376">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4359b-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4359b-377">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4359b-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="4359b-378">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4359b-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4359b-379">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4359b-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4359b-380">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4359b-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4359b-381">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4359b-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4359b-382">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4359b-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="4359b-383">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="4359b-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="4359b-384">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4359b-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="4359b-385">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4359b-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="4359b-386">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4359b-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="4359b-387">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4359b-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4359b-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4359b-389">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="4359b-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="4359b-390">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="4359b-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="4359b-391">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4359b-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-392">Az.Batch</span></span>
* <span data-ttu-id="4359b-393">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="4359b-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="4359b-394">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="4359b-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="4359b-395">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="4359b-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="4359b-396">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="4359b-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="4359b-397">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="4359b-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="4359b-398">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="4359b-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="4359b-399">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4359b-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="4359b-400">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4359b-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="4359b-401">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="4359b-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-402">Az.Compute</span></span>
* <span data-ttu-id="4359b-403">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4359b-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="4359b-404">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="4359b-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="4359b-405">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4359b-405">Breaking changes</span></span>
    - <span data-ttu-id="4359b-406">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="4359b-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="4359b-407">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="4359b-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="4359b-408">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="4359b-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="4359b-409">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4359b-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="4359b-410">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="4359b-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="4359b-411">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="4359b-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="4359b-412">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="4359b-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-413">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-414">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4359b-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-415">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-416">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4359b-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4359b-417">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4359b-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4359b-418">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="4359b-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="4359b-419">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="4359b-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4359b-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4359b-420">Az.Functions</span></span>
* <span data-ttu-id="4359b-421">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="4359b-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-422">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-423">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="4359b-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4359b-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4359b-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="4359b-425">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="4359b-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-426">Az.IotHub</span></span>
* <span data-ttu-id="4359b-427">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="4359b-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="4359b-428">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="4359b-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="4359b-429">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="4359b-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="4359b-430">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="4359b-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="4359b-431">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="4359b-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="4359b-432">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-432">New cmdlets are:</span></span>
    - <span data-ttu-id="4359b-433">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4359b-434">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4359b-435">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4359b-436">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="4359b-437">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="4359b-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="4359b-438">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="4359b-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-439">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-440">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="4359b-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="4359b-441">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4359b-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="4359b-442">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4359b-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="4359b-443">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="4359b-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="4359b-444">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="4359b-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="4359b-445">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="4359b-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="4359b-446">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="4359b-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-447">Az.Monitor</span></span>
* <span data-ttu-id="4359b-448">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="4359b-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="4359b-449">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4359b-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="4359b-450">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="4359b-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="4359b-451">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="4359b-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="4359b-452">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="4359b-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="4359b-453">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="4359b-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="4359b-454">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="4359b-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-455">Az.Network</span></span>
* <span data-ttu-id="4359b-456">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="4359b-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="4359b-457">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="4359b-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="4359b-458">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="4359b-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="4359b-459">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="4359b-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="4359b-460">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4359b-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="4359b-461">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-461">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4359b-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4359b-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4359b-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4359b-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4359b-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4359b-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4359b-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="4359b-466">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="4359b-467">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4359b-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="4359b-468">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="4359b-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="4359b-469">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4359b-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="4359b-470">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4359b-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="4359b-471">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4359b-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="4359b-472">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="4359b-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="4359b-473">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4359b-474">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4359b-475">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4359b-476">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="4359b-477">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4359b-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="4359b-478">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4359b-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="4359b-479">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="4359b-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4359b-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-482">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="4359b-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="4359b-483">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="4359b-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="4359b-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4359b-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="4359b-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4359b-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="4359b-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="4359b-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="4359b-487">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4359b-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="4359b-488">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4359b-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="4359b-489">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="4359b-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-491">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="4359b-492">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="4359b-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="4359b-493">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="4359b-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="4359b-494">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="4359b-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="4359b-495">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="4359b-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-496">Az.Resources</span></span>
* <span data-ttu-id="4359b-497">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="4359b-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="4359b-498">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="4359b-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="4359b-499">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="4359b-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="4359b-500">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="4359b-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="4359b-501">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4359b-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="4359b-502">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4359b-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="4359b-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="4359b-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="4359b-504">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="4359b-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4359b-505">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4359b-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="4359b-506">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4359b-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="4359b-507">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4359b-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="4359b-508">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="4359b-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="4359b-509">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="4359b-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="4359b-510">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4359b-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="4359b-511">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4359b-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="4359b-512">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="4359b-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="4359b-513">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="4359b-514">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="4359b-515">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4359b-516">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-518">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="4359b-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-519">Az.Sql</span></span>
* <span data-ttu-id="4359b-520">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="4359b-520">Enhance performance of:</span></span>
    - <span data-ttu-id="4359b-521">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4359b-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4359b-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4359b-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4359b-523">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4359b-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4359b-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4359b-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4359b-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4359b-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4359b-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4359b-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4359b-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4359b-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4359b-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4359b-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="4359b-529">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="4359b-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="4359b-530">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="4359b-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-531">Az.Storage</span></span>
* <span data-ttu-id="4359b-532">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-533">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="4359b-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="4359b-534">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-535">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="4359b-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="4359b-536">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4359b-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4359b-537">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="4359b-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="4359b-538">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="4359b-539">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="4359b-540">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="4359b-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="4359b-541">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="4359b-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="4359b-542">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="4359b-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="4359b-543">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="4359b-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="4359b-544">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4359b-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="4359b-545">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="4359b-546">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4359b-547">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-548">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="4359b-549">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4359b-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="4359b-550">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4359b-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4359b-551">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="4359b-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="4359b-552">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="4359b-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="4359b-553">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="4359b-554">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="4359b-555">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="4359b-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="4359b-556">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4359b-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4359b-557">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4359b-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="4359b-558">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4359b-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="4359b-559">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4359b-560">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4359b-561">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="4359b-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="4359b-562">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4359b-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4359b-563">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4359b-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="4359b-564">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4359b-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4359b-565">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4359b-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4359b-566">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4359b-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="4359b-567">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4359b-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="4359b-568">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4359b-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="4359b-569">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4359b-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="4359b-570">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="4359b-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4359b-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4359b-571">Az.TrafficManager</span></span>
* <span data-ttu-id="4359b-572">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="4359b-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-573">Az.Websites</span></span>
* <span data-ttu-id="4359b-574">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="4359b-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="4359b-575">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4359b-576">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4359b-576">Highlights since the last release</span></span>
* <span data-ttu-id="4359b-577">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4359b-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-578">Az.Accounts</span></span>
* <span data-ttu-id="4359b-579">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="4359b-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-580">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-581">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4359b-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4359b-582">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="4359b-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-583">Az.Cdn</span></span>
* <span data-ttu-id="4359b-584">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="4359b-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-586">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="4359b-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-587">Az.Compute</span></span>
* <span data-ttu-id="4359b-588">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="4359b-589">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="4359b-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-590">Az.IotHub</span></span>
* <span data-ttu-id="4359b-591">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4359b-592">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4359b-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="4359b-593">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4359b-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="4359b-594">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4359b-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="4359b-595">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4359b-596">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4359b-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="4359b-597">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4359b-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="4359b-598">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="4359b-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="4359b-599">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-599">New cmdlets are:</span></span>
    - <span data-ttu-id="4359b-600">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4359b-601">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4359b-602">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4359b-603">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="4359b-604">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4359b-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-605">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-606">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="4359b-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="4359b-607">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="4359b-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="4359b-608">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="4359b-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="4359b-609">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4359b-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4359b-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4359b-610">Az.Maintenance</span></span>
* <span data-ttu-id="4359b-611">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="4359b-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-612">Az.Monitor</span></span>
* <span data-ttu-id="4359b-613">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="4359b-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="4359b-614">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4359b-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4359b-615">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4359b-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4359b-616">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4359b-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4359b-617">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4359b-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4359b-618">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4359b-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4359b-619">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4359b-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4359b-620">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4359b-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-621">Az.Network</span></span>
* <span data-ttu-id="4359b-622">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4359b-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="4359b-623">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4359b-624">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4359b-625">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="4359b-626">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="4359b-627">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="4359b-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="4359b-628">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="4359b-629">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="4359b-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="4359b-630">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="4359b-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="4359b-631">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4359b-632">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="4359b-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="4359b-633">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="4359b-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4359b-634">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="4359b-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="4359b-635">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4359b-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="4359b-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="4359b-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-639">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="4359b-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="4359b-640">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="4359b-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-642">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="4359b-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-643">Az.Sql</span></span>
* <span data-ttu-id="4359b-644">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="4359b-645">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="4359b-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-646">Az.Storage</span></span>
* <span data-ttu-id="4359b-647">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4359b-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4359b-648">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="4359b-649">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="4359b-650">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4359b-651">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="4359b-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="4359b-652">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4359b-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4359b-653">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4359b-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4359b-654">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4359b-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="4359b-655">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4359b-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4359b-656">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="4359b-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="4359b-657">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4359b-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4359b-658">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="4359b-659">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4359b-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="4359b-660">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="4359b-661">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-661">General</span></span>
* <span data-ttu-id="4359b-662">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="4359b-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="4359b-663">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="4359b-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="4359b-664">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="4359b-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="4359b-665">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="4359b-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="4359b-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4359b-666">Az.Billing</span></span>
  - <span data-ttu-id="4359b-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-667">Az.Compute</span></span>
  - <span data-ttu-id="4359b-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4359b-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="4359b-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-669">Az.EventHub</span></span>
  - <span data-ttu-id="4359b-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-670">Az.IotHub</span></span>
  - <span data-ttu-id="4359b-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-671">Az.KeyVault</span></span>
  - <span data-ttu-id="4359b-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-672">Az.Monitor</span></span>
  - <span data-ttu-id="4359b-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-673">Az.Network</span></span>
  - <span data-ttu-id="4359b-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-674">Az.Resources</span></span>
  - <span data-ttu-id="4359b-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-675">Az.Storage</span></span>
  - <span data-ttu-id="4359b-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-676">Az.Websites</span></span>
* <span data-ttu-id="4359b-677">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="4359b-678">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4359b-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="4359b-679">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="4359b-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="4359b-680">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-681">Az.Accounts</span></span>
* <span data-ttu-id="4359b-682">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="4359b-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-683">Az.Compute</span></span>
* <span data-ttu-id="4359b-684">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="4359b-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="4359b-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="4359b-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="4359b-686">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="4359b-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="4359b-687">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="4359b-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="4359b-688">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="4359b-688">[#11354]</span></span>
* <span data-ttu-id="4359b-689">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="4359b-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="4359b-690">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4359b-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4359b-691">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4359b-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4359b-692">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4359b-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4359b-693">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4359b-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="4359b-694">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="4359b-695">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="4359b-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="4359b-696">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4359b-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="4359b-697">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="4359b-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-698">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-699">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="4359b-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="4359b-700">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="4359b-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-702">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="4359b-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="4359b-703">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="4359b-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-704">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-705">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="4359b-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-706">Az.IotHub</span></span>
* <span data-ttu-id="4359b-707">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4359b-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="4359b-708">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="4359b-709">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4359b-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="4359b-710">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4359b-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-711">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-712">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="4359b-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-713">Az.Monitor</span></span>
* <span data-ttu-id="4359b-714">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="4359b-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-715">Az.Network</span></span>
* <span data-ttu-id="4359b-716">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="4359b-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="4359b-717">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4359b-718">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4359b-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4359b-719">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4359b-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="4359b-720">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4359b-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4359b-721">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="4359b-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-723">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="4359b-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-725">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="4359b-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="4359b-726">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="4359b-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="4359b-727">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="4359b-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="4359b-728">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="4359b-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="4359b-729">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4359b-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="4359b-730">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="4359b-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-731">Az.Resources</span></span>
* <span data-ttu-id="4359b-732">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="4359b-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="4359b-733">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="4359b-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="4359b-734">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="4359b-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="4359b-735">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-735">Added example.</span></span>
* <span data-ttu-id="4359b-736">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="4359b-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="4359b-737">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="4359b-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-738">Az.Sql</span></span>
* <span data-ttu-id="4359b-739">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="4359b-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="4359b-740">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4359b-741">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="4359b-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="4359b-742">Az.Support</span></span>
* <span data-ttu-id="4359b-743">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="4359b-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-744">Az.Websites</span></span>
* <span data-ttu-id="4359b-745">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="4359b-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="4359b-746">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4359b-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4359b-747">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4359b-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4359b-748">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4359b-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4359b-749">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4359b-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="4359b-750">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-751">Az.Accounts</span></span>
* <span data-ttu-id="4359b-752">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="4359b-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="4359b-753">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="4359b-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="4359b-754">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="4359b-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-755">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-756">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="4359b-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="4359b-757">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="4359b-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="4359b-758">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="4359b-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="4359b-759">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="4359b-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-761">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="4359b-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-762">Az.IotHub</span></span>
* <span data-ttu-id="4359b-763">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4359b-764">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="4359b-765">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-766">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-767">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-768">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="4359b-769">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="4359b-770">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="4359b-771">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4359b-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="4359b-772">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4359b-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="4359b-773">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4359b-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="4359b-774">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4359b-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="4359b-775">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4359b-776">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4359b-777">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="4359b-778">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="4359b-779">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4359b-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="4359b-780">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4359b-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="4359b-781">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4359b-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-782">Az.Monitor</span></span>
* <span data-ttu-id="4359b-783">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="4359b-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-784">Az.Network</span></span>
* <span data-ttu-id="4359b-785">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="4359b-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="4359b-786">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="4359b-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="4359b-787">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="4359b-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="4359b-788">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4359b-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-789">Az.Resources</span></span>
* <span data-ttu-id="4359b-790">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="4359b-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="4359b-791">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="4359b-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="4359b-792">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="4359b-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="4359b-793">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="4359b-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="4359b-794">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="4359b-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="4359b-795">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="4359b-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="4359b-796">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="4359b-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="4359b-797">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="4359b-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4359b-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4359b-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="4359b-801">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="4359b-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="4359b-803">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="4359b-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-804">Az.Sql</span></span>
* <span data-ttu-id="4359b-805">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4359b-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4359b-806">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4359b-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="4359b-807">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4359b-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="4359b-808">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="4359b-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="4359b-809">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="4359b-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="4359b-810">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4359b-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="4359b-811">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4359b-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="4359b-812">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="4359b-813">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-814">Az.Storage</span></span>
* <span data-ttu-id="4359b-815">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="4359b-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="4359b-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="4359b-817">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4359b-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="4359b-818">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="4359b-819">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4359b-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-820">Az.Websites</span></span>
* <span data-ttu-id="4359b-821">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="4359b-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="4359b-822">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="4359b-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="4359b-823">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="4359b-824">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="4359b-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="4359b-825">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4359b-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="4359b-826">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-827">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-827">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-828">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="4359b-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="4359b-829">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4359b-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="4359b-830">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="4359b-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-831">Az.Accounts</span></span>
* <span data-ttu-id="4359b-832">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="4359b-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-833">Az.Automation</span></span>
* <span data-ttu-id="4359b-834">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4359b-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-836">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="4359b-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="4359b-837">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="4359b-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-838">Az.Compute</span></span>
* <span data-ttu-id="4359b-839">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="4359b-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-840">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-841">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="4359b-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-842">Az.IotHub</span></span>
* <span data-ttu-id="4359b-843">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4359b-844">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="4359b-845">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-846">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-847">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4359b-848">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4359b-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-849">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-850">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="4359b-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-851">Az.Monitor</span></span>
* <span data-ttu-id="4359b-852">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="4359b-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="4359b-853">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="4359b-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="4359b-854">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="4359b-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-855">Az.Network</span></span>
* <span data-ttu-id="4359b-856">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="4359b-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="4359b-857">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4359b-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4359b-858">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4359b-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4359b-859">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4359b-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="4359b-860">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-860">No new cmdlets are added.</span></span> <span data-ttu-id="4359b-861">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4359b-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-863">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4359b-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-864">Az.Resources</span></span>
* <span data-ttu-id="4359b-865">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="4359b-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="4359b-866">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4359b-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="4359b-867">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4359b-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="4359b-868">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="4359b-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="4359b-869">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4359b-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="4359b-870">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="4359b-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="4359b-871">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="4359b-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="4359b-872">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-873">Az.Sql</span></span>
* <span data-ttu-id="4359b-874">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4359b-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="4359b-875">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="4359b-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="4359b-876">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4359b-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4359b-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4359b-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4359b-878">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4359b-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4359b-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4359b-879">Az.StorageSync</span></span>
* <span data-ttu-id="4359b-880">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="4359b-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="4359b-881">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-882">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-882">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-883">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4359b-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="4359b-884">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-885">Az.Accounts</span></span>
* <span data-ttu-id="4359b-886">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="4359b-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="4359b-887">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="4359b-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-888">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-889">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="4359b-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="4359b-890">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="4359b-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="4359b-891">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="4359b-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="4359b-892">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="4359b-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-893">Az.Compute</span></span>
* <span data-ttu-id="4359b-894">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="4359b-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="4359b-895">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4359b-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="4359b-896">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4359b-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="4359b-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="4359b-898">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4359b-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-899">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-900">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="4359b-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4359b-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4359b-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="4359b-902">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="4359b-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="4359b-903">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="4359b-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-904">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-905">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="4359b-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-906">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-907">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4359b-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-908">Az.Network</span></span>
* <span data-ttu-id="4359b-909">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="4359b-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="4359b-910">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4359b-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="4359b-911">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4359b-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4359b-912">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4359b-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="4359b-913">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="4359b-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="4359b-914">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="4359b-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="4359b-915">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="4359b-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="4359b-916">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="4359b-917">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-917">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="4359b-919">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="4359b-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4359b-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="4359b-921">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="4359b-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-923">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="4359b-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="4359b-924">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4359b-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="4359b-925">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="4359b-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="4359b-926">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4359b-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-928">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="4359b-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="4359b-929">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="4359b-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-930">Az.Resources</span></span>
* <span data-ttu-id="4359b-931">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="4359b-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="4359b-932">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="4359b-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-933">Az.Sql</span></span>
<span data-ttu-id="4359b-934">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4359b-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-935">Az.Storage</span></span>
* <span data-ttu-id="4359b-936">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="4359b-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="4359b-938">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="4359b-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="4359b-939">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-940">Az.Websites</span></span>
* <span data-ttu-id="4359b-941">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="4359b-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="4359b-942">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="4359b-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="4359b-943">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4359b-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-944">Az.Accounts</span></span>
* <span data-ttu-id="4359b-945">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4359b-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-946">Az.Cdn</span></span>
* <span data-ttu-id="4359b-947">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-948">Az.Compute</span></span>
* <span data-ttu-id="4359b-949">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="4359b-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4359b-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="4359b-951">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4359b-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4359b-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4359b-953">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4359b-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4359b-954">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="4359b-955">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4359b-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4359b-956">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="4359b-957">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4359b-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4359b-958">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="4359b-959">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4359b-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4359b-960">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="4359b-961">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4359b-962">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="4359b-963">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4359b-964">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="4359b-965">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4359b-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4359b-966">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4359b-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="4359b-967">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="4359b-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="4359b-968">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="4359b-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="4359b-969">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="4359b-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="4359b-970">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="4359b-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-971">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-972">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4359b-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="4359b-973">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="4359b-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="4359b-974">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="4359b-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="4359b-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="4359b-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="4359b-976">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="4359b-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-977">Az.EventHub</span></span>
* <span data-ttu-id="4359b-978">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="4359b-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-979">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-980">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="4359b-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4359b-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4359b-981">Az.MachineLearning</span></span>
* <span data-ttu-id="4359b-982">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="4359b-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="4359b-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4359b-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="4359b-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4359b-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="4359b-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4359b-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="4359b-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4359b-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="4359b-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4359b-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="4359b-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="4359b-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="4359b-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="4359b-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-990">Az.Network</span></span>
* <span data-ttu-id="4359b-991">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="4359b-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-993">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="4359b-994">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4359b-995">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4359b-996">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-997">Az.Resources</span></span>
* <span data-ttu-id="4359b-998">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="4359b-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-999">Az.Sql</span></span>
* <span data-ttu-id="4359b-1000">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="4359b-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="4359b-1001">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="4359b-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4359b-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4359b-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4359b-1003">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="4359b-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1004">Az.Storage</span></span>
* <span data-ttu-id="4359b-1005">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4359b-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="4359b-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="4359b-1007">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4359b-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="4359b-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="4359b-1009">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="4359b-1010">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-1010">General</span></span>
* <span data-ttu-id="4359b-1011">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="4359b-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1012">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1013">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4359b-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="4359b-1014">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4359b-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-1015">Az.Batch</span></span>
* <span data-ttu-id="4359b-1016">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="4359b-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1017">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1018">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-1020">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="4359b-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="4359b-1021">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4359b-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4359b-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4359b-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="4359b-1023">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="4359b-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-1024">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-1025">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="4359b-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="4359b-1026">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="4359b-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="4359b-1027">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4359b-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-1028">Az.Monitor</span></span>
* <span data-ttu-id="4359b-1029">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4359b-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="4359b-1030">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="4359b-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="4359b-1031">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="4359b-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1032">Az.Network</span></span>
* <span data-ttu-id="4359b-1033">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="4359b-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1034">Az.Resources</span></span>
* <span data-ttu-id="4359b-1035">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="4359b-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="4359b-1036">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1037">Az.Sql</span></span>
* <span data-ttu-id="4359b-1038">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="4359b-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1039">Az.Storage</span></span>
* <span data-ttu-id="4359b-1040">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="4359b-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="4359b-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4359b-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="4359b-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4359b-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="4359b-1043">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="4359b-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="4359b-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="4359b-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="4359b-1045">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4359b-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="4359b-1046">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="4359b-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="4359b-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="4359b-1049">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="4359b-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="4359b-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4359b-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="4359b-1051">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="4359b-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="4359b-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4359b-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="4359b-1053">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-1054">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-1055">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4359b-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="4359b-1056">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4359b-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1057">Az.Compute</span></span>
* <span data-ttu-id="4359b-1058">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="4359b-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="4359b-1059">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="4359b-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="4359b-1060">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="4359b-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="4359b-1061">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="4359b-1062">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4359b-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="4359b-1063">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4359b-1064">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4359b-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="4359b-1065">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="4359b-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="4359b-1066">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4359b-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="4359b-1067">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4359b-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="4359b-1068">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4359b-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4359b-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4359b-1070">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4359b-1071">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="4359b-1071">Get the Order</span></span>
* <span data-ttu-id="4359b-1072">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4359b-1073">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="4359b-1073">Create new Order</span></span>
* <span data-ttu-id="4359b-1074">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4359b-1075">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="4359b-1075">Remove the Order</span></span>
* <span data-ttu-id="4359b-1076">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="4359b-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="4359b-1077">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="4359b-1077">Now creates Local Share</span></span>
* <span data-ttu-id="4359b-1078">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="4359b-1079">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="4359b-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="4359b-1080">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="4359b-1081">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="4359b-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="4359b-1082">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4359b-1083">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="4359b-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="4359b-1084">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4359b-1085">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="4359b-1085">Create new Triggers</span></span>
* <span data-ttu-id="4359b-1086">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4359b-1087">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="4359b-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1088">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1089">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="4359b-1090">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="4359b-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-1092">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="4359b-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1093">Az.EventHub</span></span>
* <span data-ttu-id="4359b-1094">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="4359b-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-1096">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="4359b-1097">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="4359b-1098">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="4359b-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="4359b-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1100">Az.Network</span></span>
* <span data-ttu-id="4359b-1101">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4359b-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4359b-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="4359b-1103">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1105">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="4359b-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="4359b-1106">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4359b-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="4359b-1107">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4359b-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4359b-1108">Az.RedisCache</span></span>
* <span data-ttu-id="4359b-1109">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="4359b-1110">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="4359b-1111">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="4359b-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1112">Az.Resources</span></span>
- <span data-ttu-id="4359b-1113">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4359b-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="4359b-1114">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="4359b-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="4359b-1115">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4359b-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="4359b-1116">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="4359b-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="4359b-1117">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="4359b-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1118">Az.Sql</span></span>
* <span data-ttu-id="4359b-1119">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="4359b-1120">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="4359b-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="4359b-1121">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="4359b-1122">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-1122">General</span></span>
* <span data-ttu-id="4359b-1123">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="4359b-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1124">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1125">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4359b-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4359b-1126">Az.Advisor</span></span>
* <span data-ttu-id="4359b-1127">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4359b-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-1128">Az.Batch</span></span>
* <span data-ttu-id="4359b-1129">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="4359b-1130">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="4359b-1131">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="4359b-1132">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="4359b-1133">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="4359b-1134">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="4359b-1135">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="4359b-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="4359b-1136">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4359b-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="4359b-1137">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4359b-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="4359b-1138">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4359b-1139">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="4359b-1140">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="4359b-1141">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4359b-1142">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="4359b-1143">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="4359b-1144">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="4359b-1145">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="4359b-1146">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="4359b-1147">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="4359b-1148">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4359b-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="4359b-1149">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4359b-1150">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4359b-1151">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="4359b-1152">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="4359b-1153">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="4359b-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="4359b-1154">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="4359b-1155">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="4359b-1156">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="4359b-1157">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="4359b-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="4359b-1158">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="4359b-1159">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="4359b-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="4359b-1160">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="4359b-1161">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="4359b-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="4359b-1162">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4359b-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="4359b-1163">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="4359b-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="4359b-1164">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="4359b-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-1165">Az.Cdn</span></span>
* <span data-ttu-id="4359b-1166">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="4359b-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="4359b-1167">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="4359b-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1168">Az.Compute</span></span>
* <span data-ttu-id="4359b-1169">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="4359b-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="4359b-1170">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="4359b-1171">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4359b-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="4359b-1172">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4359b-1173">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="4359b-1174">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="4359b-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="4359b-1175">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="4359b-1176">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4359b-1176">Breaking changes</span></span>
    - <span data-ttu-id="4359b-1177">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="4359b-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="4359b-1178">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4359b-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1179">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1180">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-1182">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="4359b-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="4359b-1183">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="4359b-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="4359b-1184">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="4359b-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="4359b-1185">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="4359b-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="4359b-1186">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="4359b-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="4359b-1187">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="4359b-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-1189">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="4359b-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-1190">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-1191">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="4359b-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="4359b-1192">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4359b-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="4359b-1193">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="4359b-1194">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="4359b-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="4359b-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4359b-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4359b-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4359b-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4359b-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4359b-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4359b-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="4359b-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="4359b-1200">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="4359b-1201">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4359b-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4359b-1202">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4359b-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4359b-1203">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4359b-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="4359b-1204">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="4359b-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="4359b-1205">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="4359b-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="4359b-1206">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="4359b-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="4359b-1207">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="4359b-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="4359b-1208">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4359b-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="4359b-1209">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="4359b-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="4359b-1210">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="4359b-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="4359b-1211">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="4359b-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="4359b-1212">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1213">Az.IotHub</span></span>
* <span data-ttu-id="4359b-1214">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="4359b-1214">Breaking changes:</span></span>
    - <span data-ttu-id="4359b-1215">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4359b-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4359b-1216">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4359b-1217">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4359b-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4359b-1218">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4359b-1219">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4359b-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="4359b-1220">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4359b-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="4359b-1221">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="4359b-1222">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="4359b-1223">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4359b-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4359b-1224">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4359b-1225">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4359b-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4359b-1226">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1228">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1229">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="4359b-1230">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="4359b-1231">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1232">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1233">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1234">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1235">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-1236">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="4359b-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1237">Az.Resources</span></span>
* <span data-ttu-id="4359b-1238">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="4359b-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1239">Az.Network</span></span>
* <span data-ttu-id="4359b-1240">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4359b-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="4359b-1241">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="4359b-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4359b-1247">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4359b-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="4359b-1248">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1248">New cmdlet:</span></span>
        - <span data-ttu-id="4359b-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4359b-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="4359b-1250">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="4359b-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="4359b-1251">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="4359b-1252">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="4359b-1253">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="4359b-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="4359b-1254">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="4359b-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="4359b-1255">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="4359b-1256">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="4359b-1257">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4359b-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="4359b-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4359b-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4359b-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4359b-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="4359b-1263">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4359b-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="4359b-1264">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4359b-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4359b-1265">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4359b-1266">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4359b-1267">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="4359b-1268">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="4359b-1269">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="4359b-1270">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="4359b-1272">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4359b-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4359b-1273">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4359b-1274">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4359b-1275">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4359b-1276">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4359b-1277">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="4359b-1278">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="4359b-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="4359b-1279">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="4359b-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="4359b-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4359b-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="4359b-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4359b-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="4359b-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4359b-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="4359b-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="4359b-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="4359b-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="4359b-1286">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4359b-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4359b-1287">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="4359b-1288">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="4359b-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="4359b-1289">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="4359b-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="4359b-1290">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="4359b-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="4359b-1291">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4359b-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4359b-1292">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="4359b-1293">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="4359b-1294">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="4359b-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="4359b-1295">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="4359b-1296">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="4359b-1297">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="4359b-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="4359b-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="4359b-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-1303">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="4359b-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1304">Az.Sql</span></span>
* <span data-ttu-id="4359b-1305">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="4359b-1306">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="4359b-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="4359b-1307">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="4359b-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="4359b-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4359b-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="4359b-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4359b-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="4359b-1310">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4359b-1311">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="4359b-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="4359b-1312">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="4359b-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="4359b-1313">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1314">Az.Storage</span></span>
* <span data-ttu-id="4359b-1315">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="4359b-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4359b-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4359b-1318">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="4359b-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="4359b-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4359b-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="4359b-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4359b-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="4359b-1321">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="4359b-1322">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-1322">General</span></span>
* <span data-ttu-id="4359b-1323">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1324">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1325">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="4359b-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-1327">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="4359b-1328">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="4359b-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-1329">Az.Automation</span></span>
* <span data-ttu-id="4359b-1330">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="4359b-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-1331">Az.Batch</span></span>
* <span data-ttu-id="4359b-1332">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="4359b-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1333">Az.Compute</span></span>
* <span data-ttu-id="4359b-1334">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4359b-1335">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="4359b-1336">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="4359b-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="4359b-1337">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="4359b-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1338">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1339">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="4359b-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="4359b-1340">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="4359b-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="4359b-1341">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-1343">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="4359b-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4359b-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4359b-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="4359b-1345">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="4359b-1346">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="4359b-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="4359b-1347">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="4359b-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="4359b-1348">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="4359b-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1349">Az.IotHub</span></span>
* <span data-ttu-id="4359b-1350">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4359b-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4359b-1351">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="4359b-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-1352">Az.Monitor</span></span>
* <span data-ttu-id="4359b-1353">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="4359b-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="4359b-1354">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="4359b-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="4359b-1355">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="4359b-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="4359b-1356">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4359b-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1357">Az.Network</span></span>
* <span data-ttu-id="4359b-1358">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="4359b-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="4359b-1359">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4359b-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="4359b-1360">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="4359b-1362">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4359b-1363">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4359b-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="4359b-1364">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="4359b-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4359b-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4359b-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4359b-1368">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="4359b-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="4359b-1369">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="4359b-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="4359b-1370">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4359b-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="4359b-1371">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4359b-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4359b-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4359b-1372">Az.RedisCache</span></span>
* <span data-ttu-id="4359b-1373">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="4359b-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1374">Az.Sql</span></span>
* <span data-ttu-id="4359b-1375">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4359b-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1376">Az.Storage</span></span>
* <span data-ttu-id="4359b-1377">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="4359b-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="4359b-1378">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4359b-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4359b-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4359b-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="4359b-1380">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4359b-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4359b-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4359b-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4359b-1382">Az.StorageSync</span></span>
* <span data-ttu-id="4359b-1383">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="4359b-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1384">Az.Websites</span></span>
* <span data-ttu-id="4359b-1385">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="4359b-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="4359b-1386">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4359b-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-1388">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4359b-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4359b-1389">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="4359b-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4359b-1390">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-1391">Az.Automation</span></span>
* <span data-ttu-id="4359b-1392">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="4359b-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4359b-1393">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="4359b-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4359b-1394">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="4359b-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1395">Az.Compute</span></span>
* <span data-ttu-id="4359b-1396">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4359b-1397">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4359b-1398">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="4359b-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4359b-1399">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4359b-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4359b-1400">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4359b-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4359b-1401">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4359b-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4359b-1402">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="4359b-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4359b-1403">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="4359b-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4359b-1404">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4359b-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1405">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1406">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4359b-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4359b-1407">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="4359b-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-1408">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-1409">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="4359b-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1410">Az.IotHub</span></span>
* <span data-ttu-id="4359b-1411">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="4359b-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4359b-1412">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="4359b-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4359b-1413">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4359b-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="4359b-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4359b-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4359b-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4359b-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4359b-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4359b-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4359b-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4359b-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-1418">Az.Monitor</span></span>
* <span data-ttu-id="4359b-1419">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="4359b-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4359b-1420">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="4359b-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4359b-1421">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="4359b-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4359b-1422">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4359b-1423">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="4359b-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4359b-1424">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="4359b-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4359b-1425">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4359b-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4359b-1426">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4359b-1427">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4359b-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4359b-1428">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4359b-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4359b-1429">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4359b-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4359b-1430">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4359b-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4359b-1431">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4359b-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4359b-1432">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4359b-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4359b-1433">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4359b-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4359b-1434">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4359b-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4359b-1435">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="4359b-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4359b-1436">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4359b-1437">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="4359b-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4359b-1438">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-1438">Overall improved help files</span></span>
* <span data-ttu-id="4359b-1439">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="4359b-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1440">Az.Network</span></span>
* <span data-ttu-id="4359b-1441">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="4359b-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="4359b-1442">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="4359b-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4359b-1443">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="4359b-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4359b-1444">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="4359b-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4359b-1445">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="4359b-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4359b-1446">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="4359b-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4359b-1447">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="4359b-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4359b-1448">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4359b-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4359b-1449">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4359b-1450">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="4359b-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4359b-1451">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4359b-1452">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="4359b-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4359b-1453">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1453">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4359b-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4359b-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4359b-1456">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="4359b-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4359b-1457">New-VpnSite</span></span>
        - <span data-ttu-id="4359b-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4359b-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="4359b-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="4359b-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="4359b-1461">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4359b-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1463">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="4359b-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4359b-1464">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="4359b-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1465">Az.Resources</span></span>
* <span data-ttu-id="4359b-1466">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="4359b-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-1468">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4359b-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4359b-1469">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="4359b-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4359b-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4359b-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4359b-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4359b-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4359b-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4359b-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4359b-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4359b-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4359b-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4359b-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4359b-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4359b-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4359b-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4359b-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4359b-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4359b-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4359b-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4359b-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4359b-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4359b-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4359b-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4359b-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4359b-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4359b-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4359b-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4359b-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4359b-1483">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4359b-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4359b-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4359b-1484">Az.SignalR</span></span>
* <span data-ttu-id="4359b-1485">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="4359b-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1486">Az.Sql</span></span>
* <span data-ttu-id="4359b-1487">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="4359b-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4359b-1488">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="4359b-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4359b-1489">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4359b-1490">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4359b-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4359b-1491">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4359b-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1492">Az.Storage</span></span>
* <span data-ttu-id="4359b-1493">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4359b-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4359b-1494">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="4359b-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4359b-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4359b-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4359b-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4359b-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4359b-1497">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="4359b-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4359b-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4359b-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4359b-1499">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4359b-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4359b-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4359b-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4359b-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4359b-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4359b-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1504">Az.Websites</span></span>
* <span data-ttu-id="4359b-1505">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="4359b-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4359b-1506">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="4359b-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4359b-1507">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="4359b-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4359b-1508">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4359b-1509">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-1509">General</span></span>
* <span data-ttu-id="4359b-1510">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="4359b-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1511">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1512">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="4359b-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4359b-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4359b-1513">Az.Aks</span></span>
* <span data-ttu-id="4359b-1514">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="4359b-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4359b-1515">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4359b-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-1517">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4359b-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4359b-1518">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="4359b-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4359b-1519">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="4359b-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4359b-1520">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4359b-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4359b-1521">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4359b-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-1522">Az.Batch</span></span>
* <span data-ttu-id="4359b-1523">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="4359b-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-1524">Az.Cdn</span></span>
* <span data-ttu-id="4359b-1525">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="4359b-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1526">Az.Compute</span></span>
* <span data-ttu-id="4359b-1527">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4359b-1528">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4359b-1529">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="4359b-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4359b-1530">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4359b-1531">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4359b-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4359b-1532">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4359b-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4359b-1533">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4359b-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4359b-1534">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="4359b-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1535">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1536">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="4359b-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4359b-1537">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="4359b-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4359b-1538">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4359b-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4359b-1539">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="4359b-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-1541">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="4359b-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1542">Az.EventHub</span></span>
* <span data-ttu-id="4359b-1543">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4359b-1544">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="4359b-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4359b-1545">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4359b-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4359b-1546">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4359b-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4359b-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4359b-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4359b-1548">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="4359b-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-1549">Az.Monitor</span></span>
* <span data-ttu-id="4359b-1550">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1551">Az.Network</span></span>
* <span data-ttu-id="4359b-1552">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4359b-1553">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4359b-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4359b-1554">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="4359b-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4359b-1555">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="4359b-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4359b-1556">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="4359b-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="4359b-1557">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4359b-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4359b-1558">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4359b-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-1560">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="4359b-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4359b-1561">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="4359b-1561">Added example</span></span>
    - <span data-ttu-id="4359b-1562">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="4359b-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4359b-1563">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4359b-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4359b-1564">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4359b-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1566">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1567">Az.Resources</span></span>
* <span data-ttu-id="4359b-1568">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="4359b-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4359b-1569">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="4359b-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4359b-1570">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="4359b-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4359b-1571">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-1573">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4359b-1574">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4359b-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4359b-1575">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="4359b-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-1577">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="4359b-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4359b-1578">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4359b-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4359b-1579">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4359b-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4359b-1580">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="4359b-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4359b-1581">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4359b-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4359b-1582">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4359b-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1583">Az.Sql</span></span>
* <span data-ttu-id="4359b-1584">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4359b-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1585">Az.Storage</span></span>
* <span data-ttu-id="4359b-1586">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4359b-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4359b-1587">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="4359b-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4359b-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4359b-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4359b-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4359b-1590">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="4359b-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4359b-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1592">Az.Websites</span></span>
* <span data-ttu-id="4359b-1593">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4359b-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4359b-1594">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1595">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1596">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4359b-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4359b-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4359b-1598">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="4359b-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-1599">Az.Automation</span></span>
* <span data-ttu-id="4359b-1600">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="4359b-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-1602">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4359b-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1603">Az.Compute</span></span>
* <span data-ttu-id="4359b-1604">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="4359b-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4359b-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4359b-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4359b-1606">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="4359b-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4359b-1607">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4359b-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1608">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1609">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4359b-1610">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="4359b-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1611">Az.EventHub</span></span>
* <span data-ttu-id="4359b-1612">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4359b-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4359b-1613">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4359b-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-1614">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-1615">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4359b-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4359b-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4359b-1616">Az.LogicApp</span></span>
* <span data-ttu-id="4359b-1617">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="4359b-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4359b-1618">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="4359b-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4359b-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="4359b-1620">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="4359b-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1621">Az.Network</span></span>
* <span data-ttu-id="4359b-1622">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="4359b-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4359b-1623">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1623">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4359b-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4359b-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4359b-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4359b-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4359b-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4359b-1632">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="4359b-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4359b-1633">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="4359b-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4359b-1634">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4359b-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4359b-1635">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4359b-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4359b-1636">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4359b-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4359b-1637">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4359b-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4359b-1638">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4359b-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="4359b-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4359b-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4359b-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4359b-1642">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4359b-1643">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4359b-1644">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="4359b-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4359b-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4359b-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4359b-1648">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="4359b-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4359b-1649">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="4359b-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4359b-1650">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="4359b-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-1652">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="4359b-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="4359b-1653">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="4359b-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1655">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4359b-1656">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4359b-1657">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4359b-1658">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4359b-1659">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4359b-1660">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4359b-1661">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4359b-1662">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4359b-1663">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4359b-1664">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="4359b-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1665">Az.Resources</span></span>
- <span data-ttu-id="4359b-1666">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4359b-1667">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4359b-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-1669">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4359b-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4359b-1670">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4359b-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1671">Az.Sql</span></span>
* <span data-ttu-id="4359b-1672">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4359b-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4359b-1673">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="4359b-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4359b-1674">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="4359b-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1675">Az.Storage</span></span>
* <span data-ttu-id="4359b-1676">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4359b-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4359b-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4359b-1677">Az.StorageSync</span></span>
* <span data-ttu-id="4359b-1678">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="4359b-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4359b-1679">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4359b-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1680">Az.Websites</span></span>
* <span data-ttu-id="4359b-1681">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4359b-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4359b-1682">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4359b-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4359b-1683">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4359b-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4359b-1684">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1685">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1686">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="4359b-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4359b-1687">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="4359b-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4359b-1688">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4359b-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4359b-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4359b-1689">Az.Advisor</span></span>
* <span data-ttu-id="4359b-1690">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4359b-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4359b-1691">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4359b-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4359b-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-1693">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4359b-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4359b-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4359b-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4359b-1695">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="4359b-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4359b-1696">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="4359b-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4359b-1697">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4359b-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4359b-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4359b-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4359b-1699">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="4359b-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-1700">Az.Automation</span></span>
* <span data-ttu-id="4359b-1701">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4359b-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1702">Az.Compute</span></span>
* <span data-ttu-id="4359b-1703">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-1704">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-1705">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="4359b-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4359b-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4359b-1706">Az.EventGrid</span></span>
* <span data-ttu-id="4359b-1707">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="4359b-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1708">Az.IotHub</span></span>
* <span data-ttu-id="4359b-1709">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="4359b-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1710">Az.Network</span></span>
* <span data-ttu-id="4359b-1711">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="4359b-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4359b-1712">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="4359b-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-1714">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4359b-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4359b-1715">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4359b-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-1717">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4359b-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1719">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="4359b-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1720">Az.Resources</span></span>
    - <span data-ttu-id="4359b-1721">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="4359b-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4359b-1722">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4359b-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4359b-1723">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4359b-1724">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="4359b-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-1726">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4359b-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1727">Az.Sql</span></span>
* <span data-ttu-id="4359b-1728">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="4359b-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4359b-1729">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4359b-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4359b-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4359b-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4359b-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4359b-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4359b-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4359b-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4359b-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4359b-1736">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="4359b-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1737">Az.Storage</span></span>
* <span data-ttu-id="4359b-1738">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4359b-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4359b-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4359b-1740">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="4359b-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4359b-1741">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="4359b-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4359b-1742">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4359b-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4359b-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4359b-1745">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="4359b-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4359b-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4359b-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4359b-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4359b-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4359b-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4359b-1748">Az.StorageSync</span></span>
* <span data-ttu-id="4359b-1749">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4359b-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4359b-1750">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-1751">Az.Accounts</span></span>
* <span data-ttu-id="4359b-1752">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="4359b-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4359b-1753">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4359b-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4359b-1754">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="4359b-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4359b-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4359b-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4359b-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4359b-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1757">Az.Compute</span></span>
* <span data-ttu-id="4359b-1758">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4359b-1759">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4359b-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4359b-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4359b-1760">Az.Dns</span></span>
* <span data-ttu-id="4359b-1761">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4359b-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4359b-1762">Az.EventGrid</span></span>
* <span data-ttu-id="4359b-1763">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4359b-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4359b-1764">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4359b-1764">New cmdlets:</span></span>
    - <span data-ttu-id="4359b-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4359b-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4359b-1766">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4359b-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4359b-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4359b-1768">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4359b-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4359b-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4359b-1770">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4359b-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4359b-1772">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4359b-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4359b-1774">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4359b-1775">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4359b-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4359b-1776">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4359b-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4359b-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4359b-1778">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="4359b-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="4359b-1779">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4359b-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4359b-1780">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="4359b-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4359b-1781">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4359b-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="4359b-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4359b-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4359b-1783">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4359b-1784">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4359b-1785">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="4359b-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4359b-1786">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4359b-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4359b-1787">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="4359b-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4359b-1788">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="4359b-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4359b-1789">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="4359b-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4359b-1790">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="4359b-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="4359b-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4359b-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4359b-1792">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4359b-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4359b-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4359b-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4359b-1794">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4359b-1795">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4359b-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4359b-1798">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4359b-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4359b-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4359b-1800">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4359b-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1801">Az.Network</span></span>
* <span data-ttu-id="4359b-1802">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4359b-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4359b-1803">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1803">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4359b-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4359b-1805">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4359b-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4359b-1806">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1806">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4359b-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4359b-1808">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4359b-1809">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1809">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4359b-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4359b-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4359b-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4359b-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4359b-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4359b-1815">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4359b-1816">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-1816">New cmdlets</span></span>
        - <span data-ttu-id="4359b-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4359b-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4359b-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4359b-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4359b-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4359b-1821">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4359b-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4359b-1822">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4359b-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4359b-1823">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4359b-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4359b-1824">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4359b-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4359b-1825">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4359b-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4359b-1826">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4359b-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4359b-1827">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4359b-1828">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="4359b-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4359b-1829">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4359b-1830">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="4359b-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4359b-1831">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4359b-1832">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4359b-1833">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4359b-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4359b-1834">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4359b-1835">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4359b-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4359b-1836">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4359b-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4359b-1837">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4359b-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4359b-1838">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="4359b-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4359b-1839">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4359b-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="4359b-1840">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4359b-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="4359b-1841">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4359b-1842">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4359b-1843">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-1845">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4359b-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1846">Az.Resources</span></span>
* <span data-ttu-id="4359b-1847">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="4359b-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4359b-1848">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4359b-1849">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4359b-1850">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="4359b-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-1852">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="4359b-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1853">Az.Sql</span></span>
* <span data-ttu-id="4359b-1854">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4359b-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4359b-1855">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4359b-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4359b-1856">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4359b-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4359b-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4359b-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4359b-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4359b-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4359b-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4359b-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4359b-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4359b-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-1862">Az.Storage</span></span>
* <span data-ttu-id="4359b-1863">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4359b-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="4359b-1865">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="4359b-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4359b-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1867">Az.Websites</span></span>
* <span data-ttu-id="4359b-1868">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="4359b-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4359b-1869">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4359b-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4359b-1870">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4359b-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-1871">Az.Cdn</span></span>
* <span data-ttu-id="4359b-1872">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="4359b-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1873">Az.Compute</span></span>
* <span data-ttu-id="4359b-1874">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4359b-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4359b-1875">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4359b-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-1876">Az.EventHub</span></span>
* <span data-ttu-id="4359b-1877">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="4359b-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4359b-1878">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4359b-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1879">Az.Network</span></span>
* <span data-ttu-id="4359b-1880">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="4359b-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4359b-1881">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="4359b-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-1883">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4359b-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-1885">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="4359b-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-1887">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4359b-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-1889">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4359b-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4359b-1890">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1891">Az.Sql</span></span>
* <span data-ttu-id="4359b-1892">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4359b-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4359b-1893">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4359b-1894">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4359b-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4359b-1895">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4359b-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-1896">Az.Websites</span></span>
* <span data-ttu-id="4359b-1897">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="4359b-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4359b-1898">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4359b-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-1900">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4359b-1901">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4359b-1902">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4359b-1903">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="4359b-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4359b-1904">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4359b-1905">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4359b-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4359b-1906">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4359b-1907">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4359b-1908">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4359b-1909">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="4359b-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4359b-1910">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4359b-1911">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="4359b-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4359b-1912">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="4359b-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4359b-1913">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="4359b-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4359b-1914">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="4359b-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4359b-1915">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="4359b-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4359b-1916">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4359b-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4359b-1917">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4359b-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4359b-1918">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="4359b-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="4359b-1919">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="4359b-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4359b-1920">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="4359b-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4359b-1921">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="4359b-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4359b-1922">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="4359b-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4359b-1923">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="4359b-1924">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4359b-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4359b-1925">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4359b-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4359b-1926">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4359b-1927">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4359b-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4359b-1928">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4359b-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4359b-1929">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="4359b-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4359b-1930">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="4359b-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="4359b-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4359b-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4359b-1932">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4359b-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4359b-1933">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4359b-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4359b-1934">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4359b-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4359b-1935">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="4359b-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4359b-1936">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="4359b-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4359b-1937">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="4359b-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4359b-1938">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="4359b-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4359b-1939">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4359b-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4359b-1940">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4359b-1941">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4359b-1942">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4359b-1943">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4359b-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4359b-1944">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4359b-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4359b-1945">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4359b-1946">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4359b-1947">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4359b-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4359b-1948">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="4359b-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4359b-1949">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4359b-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4359b-1950">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="4359b-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4359b-1951">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="4359b-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4359b-1952">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="4359b-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4359b-1953">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="4359b-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4359b-1954">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="4359b-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4359b-1955">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="4359b-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4359b-1956">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4359b-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4359b-1957">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4359b-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4359b-1958">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4359b-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4359b-1959">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4359b-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4359b-1960">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4359b-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4359b-1961">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4359b-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4359b-1962">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4359b-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4359b-1963">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4359b-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4359b-1964">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="4359b-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4359b-1965">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="4359b-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4359b-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4359b-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4359b-1967">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="4359b-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4359b-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4359b-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4359b-1969">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4359b-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4359b-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4359b-1971">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4359b-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4359b-1972">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="4359b-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4359b-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4359b-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4359b-1974">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="4359b-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="4359b-1975">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4359b-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4359b-1976">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="4359b-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-1977">Az.Automation</span></span>
* <span data-ttu-id="4359b-1978">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="4359b-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4359b-1979">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4359b-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4359b-1980">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4359b-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4359b-1981">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="4359b-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4359b-1982">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4359b-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4359b-1983">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="4359b-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4359b-1984">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="4359b-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-1985">Az.Compute</span></span>
* <span data-ttu-id="4359b-1986">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4359b-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4359b-1987">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="4359b-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-1989">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-1990">Az.Monitor</span></span>
* <span data-ttu-id="4359b-1991">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-1992">Az.Network</span></span>
* <span data-ttu-id="4359b-1993">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="4359b-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4359b-1994">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4359b-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="4359b-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4359b-1996">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4359b-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-1997">Az.Resources</span></span>
* <span data-ttu-id="4359b-1998">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="4359b-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-1999">Az.Sql</span></span>
* <span data-ttu-id="4359b-2000">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="4359b-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4359b-2001">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2002">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2003">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="4359b-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-2005">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="4359b-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4359b-2006">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="4359b-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2007">Az.Compute</span></span>
* <span data-ttu-id="4359b-2008">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="4359b-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4359b-2009">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4359b-2010">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4359b-2011">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4359b-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4359b-2012">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4359b-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4359b-2013">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="4359b-2014">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4359b-2014">Breaking changes</span></span>
    - <span data-ttu-id="4359b-2015">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4359b-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4359b-2016">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4359b-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4359b-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4359b-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="4359b-2018">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4359b-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4359b-2019">Az.Dns</span></span>
* <span data-ttu-id="4359b-2020">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="4359b-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4359b-2021">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="4359b-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4359b-2022">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="4359b-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4359b-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="4359b-2024">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4359b-2025">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="4359b-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4359b-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-2026">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-2027">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4359b-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4359b-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4359b-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4359b-2030">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4359b-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4359b-2031">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="4359b-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4359b-2032">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="4359b-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4359b-2033">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="4359b-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-2034">Az.Monitor</span></span>
* <span data-ttu-id="4359b-2035">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4359b-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="4359b-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4359b-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4359b-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4359b-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4359b-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4359b-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4359b-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4359b-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4359b-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4359b-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4359b-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4359b-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4359b-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4359b-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4359b-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4359b-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4359b-2047">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="4359b-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4359b-2048">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4359b-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2049">Az.Network</span></span>
* <span data-ttu-id="4359b-2050">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="4359b-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4359b-2051">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4359b-2051">New cmdlets</span></span>
        - <span data-ttu-id="4359b-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="4359b-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4359b-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4359b-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4359b-2056">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4359b-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="4359b-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4359b-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4359b-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4359b-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4359b-2059">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="4359b-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4359b-2060">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4359b-2061">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4359b-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-2063">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="4359b-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4359b-2064">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="4359b-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4359b-2065">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="4359b-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-2067">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4359b-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4359b-2068">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4359b-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4359b-2069">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4359b-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4359b-2070">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4359b-2071">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4359b-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4359b-2072">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="4359b-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4359b-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4359b-2073">Az.Relay</span></span>
* <span data-ttu-id="4359b-2074">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="4359b-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-2076">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4359b-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2077">Az.Storage</span></span>
* <span data-ttu-id="4359b-2078">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="4359b-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4359b-2079">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="4359b-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4359b-2080">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="4359b-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4359b-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="4359b-2082">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="4359b-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4359b-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4359b-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4359b-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2086">Az.Websites</span></span>
* <span data-ttu-id="4359b-2087">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4359b-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4359b-2088">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="4359b-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4359b-2089">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-2090">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-2091">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4359b-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="4359b-2092">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4359b-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4359b-2093">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4359b-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4359b-2094">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4359b-2095">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4359b-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4359b-2096">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4359b-2097">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4359b-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2098">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2099">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="4359b-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4359b-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-2100">Az.Batch</span></span>
* <span data-ttu-id="4359b-2101">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-2102">Az.Cdn</span></span>
* <span data-ttu-id="4359b-2103">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-2105">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2106">Az.Compute</span></span>
* <span data-ttu-id="4359b-2107">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="4359b-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4359b-2108">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2109">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4359b-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-2110">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-2111">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4359b-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2113">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4359b-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4359b-2114">Az.EventGrid</span></span>
* <span data-ttu-id="4359b-2115">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="4359b-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2116">Az.EventHub</span></span>
* <span data-ttu-id="4359b-2117">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4359b-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4359b-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4359b-2118">Az.HDInsight</span></span>
* <span data-ttu-id="4359b-2119">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2120">Az.IotHub</span></span>
* <span data-ttu-id="4359b-2121">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2122">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-2123">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2124">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4359b-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4359b-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4359b-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="4359b-2126">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4359b-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4359b-2127">Az.Media</span></span>
* <span data-ttu-id="4359b-2128">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-2129">Az.Monitor</span></span>
  * <span data-ttu-id="4359b-2130">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4359b-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4359b-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4359b-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4359b-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4359b-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4359b-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4359b-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4359b-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4359b-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4359b-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4359b-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4359b-2136">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="4359b-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2137">Az.Network</span></span>
* <span data-ttu-id="4359b-2138">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2139">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4359b-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4359b-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4359b-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="4359b-2141">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-2143">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4359b-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4359b-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4359b-2145">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-2147">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2148">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4359b-2149">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4359b-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4359b-2150">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="4359b-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4359b-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4359b-2151">Az.RedisCache</span></span>
* <span data-ttu-id="4359b-2152">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2153">Az.Resources</span></span>
* <span data-ttu-id="4359b-2154">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4359b-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2155">Az.Sql</span></span>
* <span data-ttu-id="4359b-2156">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="4359b-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4359b-2157">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2158">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="4359b-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4359b-2159">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="4359b-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4359b-2160">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="4359b-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4359b-2161">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4359b-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4359b-2162">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4359b-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2163">Az.Websites</span></span>
* <span data-ttu-id="4359b-2164">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="4359b-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4359b-2165">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4359b-2166">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="4359b-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4359b-2167">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4359b-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4359b-2168">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-2169">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-2170">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4359b-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="4359b-2171">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4359b-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4359b-2172">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4359b-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4359b-2173">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4359b-2174">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4359b-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4359b-2175">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4359b-2176">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4359b-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4359b-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2177">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2178">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4359b-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="4359b-2180">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="4359b-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4359b-2181">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="4359b-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2182">Az.Automation</span></span>
* <span data-ttu-id="4359b-2183">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="4359b-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4359b-2184">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="4359b-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4359b-2185">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2186">Az.Compute</span></span>
* <span data-ttu-id="4359b-2187">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4359b-2188">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="4359b-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4359b-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="4359b-2190">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="4359b-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-2191">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-2192">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="4359b-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4359b-2193">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4359b-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2194">Az.Resources</span></span>
* <span data-ttu-id="4359b-2195">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="4359b-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4359b-2196">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4359b-2197">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="4359b-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4359b-2198">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4359b-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4359b-2199">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="4359b-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4359b-2200">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4359b-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2201">Az.Sql</span></span>
* <span data-ttu-id="4359b-2202">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="4359b-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2203">Az.Storage</span></span>
* <span data-ttu-id="4359b-2204">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4359b-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4359b-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="4359b-2206">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4359b-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4359b-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4359b-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4359b-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4359b-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4359b-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4359b-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4359b-2211">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="4359b-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4359b-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4359b-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4359b-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4359b-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4359b-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4359b-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4359b-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4359b-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4359b-2216">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4359b-2217">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4359b-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="4359b-2218">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4359b-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="4359b-2219">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4359b-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4359b-2220">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4359b-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4359b-2221">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4359b-2222">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4359b-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4359b-2223">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4359b-2224">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4359b-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2225">Az.Automation</span></span>
* <span data-ttu-id="4359b-2226">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="4359b-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4359b-2227">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="4359b-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="4359b-2228">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="4359b-2228">Pre-Post script</span></span>
    * <span data-ttu-id="4359b-2229">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="4359b-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2230">Az.Compute</span></span>
* <span data-ttu-id="4359b-2231">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4359b-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4359b-2232">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4359b-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2233">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-2234">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2235">Az.Network</span></span>
* <span data-ttu-id="4359b-2236">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4359b-2237">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="4359b-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-2239">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="4359b-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4359b-2240">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="4359b-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2241">Az.Resources</span></span>
* <span data-ttu-id="4359b-2242">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4359b-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4359b-2243">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="4359b-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2244">Az.Sql</span></span>
* <span data-ttu-id="4359b-2245">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="4359b-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2246">Az.Storage</span></span>
* <span data-ttu-id="4359b-2247">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4359b-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4359b-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4359b-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4359b-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4359b-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4359b-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4359b-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4359b-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2254">Az.Websites</span></span>
* <span data-ttu-id="4359b-2255">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="4359b-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="4359b-2256">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2257">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2258">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="4359b-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4359b-2259">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2260">Az.Automation</span></span>
* <span data-ttu-id="4359b-2261">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4359b-2262">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="4359b-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4359b-2263">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="4359b-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-2264">Az.Cdn</span></span>
* <span data-ttu-id="4359b-2265">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="4359b-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2266">Az.Compute</span></span>
* <span data-ttu-id="4359b-2267">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="4359b-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-2268">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-2269">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4359b-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4359b-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4359b-2270">Az.LogicApp</span></span>
* <span data-ttu-id="4359b-2271">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="4359b-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2272">Az.Network</span></span>
* <span data-ttu-id="4359b-2273">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-2275">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4359b-2276">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="4359b-2276">SDK Update</span></span>
* <span data-ttu-id="4359b-2277">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4359b-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4359b-2278">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4359b-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2279">Az.Resources</span></span>
* <span data-ttu-id="4359b-2280">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4359b-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4359b-2281">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4359b-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4359b-2282">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4359b-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4359b-2283">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4359b-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4359b-2284">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4359b-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4359b-2285">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4359b-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2286">Az.Sql</span></span>
* <span data-ttu-id="4359b-2287">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="4359b-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4359b-2288">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4359b-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2289">Az.Storage</span></span>
* <span data-ttu-id="4359b-2290">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4359b-2291">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="4359b-2293">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2294">Az.Automation</span></span>
* <span data-ttu-id="4359b-2295">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4359b-2296">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4359b-2297">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-2299">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="4359b-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2300">Az.Compute</span></span>
* <span data-ttu-id="4359b-2301">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="4359b-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4359b-2302">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="4359b-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4359b-2303">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4359b-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4359b-2304">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="4359b-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2306">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="4359b-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4359b-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2307">Az.EventHub</span></span>
* <span data-ttu-id="4359b-2308">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2309">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-2310">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4359b-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4359b-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4359b-2311">Az.LogicApp</span></span>
* <span data-ttu-id="4359b-2312">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="4359b-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4359b-2313">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="4359b-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4359b-2314">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="4359b-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4359b-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4359b-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4359b-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4359b-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4359b-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4359b-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4359b-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4359b-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4359b-2319">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="4359b-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4359b-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4359b-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4359b-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4359b-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4359b-2324">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4359b-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4359b-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-2325">Az.Monitor</span></span>
* <span data-ttu-id="4359b-2326">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="4359b-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2327">Az.Network</span></span>
* <span data-ttu-id="4359b-2328">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4359b-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="4359b-2330">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="4359b-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4359b-2331">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="4359b-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="4359b-2332">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="4359b-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2333">Az.Resources</span></span>
* <span data-ttu-id="4359b-2334">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4359b-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4359b-2335">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4359b-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4359b-2336">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4359b-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4359b-2337">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="4359b-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2338">Az.Sql</span></span>
* <span data-ttu-id="4359b-2339">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4359b-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4359b-2340">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="4359b-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2341">Az.Websites</span></span>
* <span data-ttu-id="4359b-2342">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4359b-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4359b-2343">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2344">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2345">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4359b-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="4359b-2347">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="4359b-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2348">Az.Compute</span></span>
* <span data-ttu-id="4359b-2349">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="4359b-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4359b-2350">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4359b-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4359b-2351">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4359b-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="4359b-2353">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="4359b-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2354">Az.Resources</span></span>
* <span data-ttu-id="4359b-2355">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4359b-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="4359b-2356">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4359b-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4359b-2357">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4359b-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="4359b-2358">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4359b-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2359">Az.Sql</span></span>
* <span data-ttu-id="4359b-2360">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4359b-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4359b-2361">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="4359b-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4359b-2362">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4359b-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4359b-2363">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2364">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2365">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="4359b-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4359b-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="4359b-2367">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="4359b-2369">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4359b-2370">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2371">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2372">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4359b-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4359b-2373">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4359b-2374">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4359b-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4359b-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4359b-2375">Az.Aks</span></span>
* <span data-ttu-id="4359b-2376">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4359b-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2377">Az.Automation</span></span>
* <span data-ttu-id="4359b-2378">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="4359b-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4359b-2379">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4359b-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4359b-2380">Az.Cdn</span></span>
* <span data-ttu-id="4359b-2381">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2382">Az.Compute</span></span>
* <span data-ttu-id="4359b-2383">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4359b-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4359b-2384">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4359b-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4359b-2385">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4359b-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4359b-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4359b-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4359b-2387">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4359b-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4359b-2388">Az.DataFactory</span></span>
* <span data-ttu-id="4359b-2389">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4359b-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2391">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4359b-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4359b-2392">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4359b-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4359b-2393">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2394">Az.IotHub</span></span>
* <span data-ttu-id="4359b-2395">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4359b-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4359b-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2396">Az.KeyVault</span></span>
* <span data-ttu-id="4359b-2397">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2398">Az.Network</span></span>
* <span data-ttu-id="4359b-2399">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2400">Az.Resources</span></span>
* <span data-ttu-id="4359b-2401">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="4359b-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4359b-2402">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4359b-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4359b-2403">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4359b-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4359b-2404">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4359b-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4359b-2405">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4359b-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4359b-2406">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4359b-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4359b-2407">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4359b-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-2409">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4359b-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4359b-2410">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="4359b-2410">Fix some error messages.</span></span>
* <span data-ttu-id="4359b-2411">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="4359b-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4359b-2412">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="4359b-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4359b-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4359b-2413">Az.SignalR</span></span>
* <span data-ttu-id="4359b-2414">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2415">Az.Sql</span></span>
* <span data-ttu-id="4359b-2416">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4359b-2417">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4359b-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4359b-2418">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="4359b-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4359b-2419">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4359b-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2420">Az.Storage</span></span>
* <span data-ttu-id="4359b-2421">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4359b-2422">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4359b-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4359b-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4359b-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4359b-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4359b-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4359b-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="4359b-2426">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2427">Az.Websites</span></span>
* <span data-ttu-id="4359b-2428">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4359b-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4359b-2429">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="4359b-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4359b-2430">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4359b-2431">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4359b-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4359b-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2432">Az.Accounts</span></span>
* <span data-ttu-id="4359b-2433">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4359b-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2434">Az.Compute</span></span>
* <span data-ttu-id="4359b-2435">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4359b-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4359b-2436">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4359b-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4359b-2437">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2439">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="4359b-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4359b-2440">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="4359b-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4359b-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4359b-2441">Az.EventGrid</span></span>
* <span data-ttu-id="4359b-2442">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4359b-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4359b-2443">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4359b-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4359b-2444">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4359b-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4359b-2445">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4359b-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4359b-2446">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4359b-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4359b-2447">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4359b-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4359b-2448">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4359b-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4359b-2449">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4359b-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4359b-2450">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4359b-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4359b-2451">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4359b-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="4359b-2452">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4359b-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4359b-2453">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="4359b-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4359b-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2454">Az.IotHub</span></span>
* <span data-ttu-id="4359b-2455">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="4359b-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4359b-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4359b-2456">Az.LogicApp</span></span>
* <span data-ttu-id="4359b-2457">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="4359b-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2458">Az.Resources</span></span>
* <span data-ttu-id="4359b-2459">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="4359b-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4359b-2460">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4359b-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4359b-2461">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4359b-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4359b-2462">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4359b-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4359b-2463">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="4359b-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4359b-2464">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4359b-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4359b-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4359b-2465">Az.SignalR</span></span>
* <span data-ttu-id="4359b-2466">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2467">Az.Sql</span></span>
* <span data-ttu-id="4359b-2468">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="4359b-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4359b-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2469">Az.Storage</span></span>
* <span data-ttu-id="4359b-2470">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="4359b-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4359b-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4359b-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="4359b-2472">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="4359b-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4359b-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4359b-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2474">Az.Websites</span></span>
* <span data-ttu-id="4359b-2475">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4359b-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4359b-2476">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4359b-2477">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4359b-2478">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-2478">General</span></span>

- <span data-ttu-id="4359b-2479">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="4359b-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="4359b-2480">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="4359b-2480">Online help for each module</span></span>
- <span data-ttu-id="4359b-2481">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4359b-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4359b-2482">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4359b-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4359b-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2483">Az.Accounts</span></span>
- <span data-ttu-id="4359b-2484">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4359b-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="4359b-2485">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="4359b-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4359b-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="4359b-2487">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="4359b-2487">Fixes for #7002</span></span>
- <span data-ttu-id="4359b-2488">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4359b-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4359b-2489">Az.Batch</span></span>
- <span data-ttu-id="4359b-2490">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4359b-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4359b-2491">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="4359b-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4359b-2492">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4359b-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4359b-2493">Az.Billing</span></span>
- <span data-ttu-id="4359b-2494">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4359b-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="4359b-2496">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4359b-2497">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4359b-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4359b-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="4359b-2499">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4359b-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4359b-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4359b-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4359b-2501">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="4359b-2503">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4359b-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4359b-2504">Az.Monitor</span></span>
- <span data-ttu-id="4359b-2505">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4359b-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4359b-2506">Az.KeyVault</span></span>
- <span data-ttu-id="4359b-2507">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="4359b-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4359b-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4359b-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="4359b-2509">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4359b-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4359b-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4359b-2510">Az.Media</span></span>
- <span data-ttu-id="4359b-2511">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4359b-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4359b-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2512">Az.Network</span></span>
<span data-ttu-id="4359b-2513">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4359b-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4359b-2514">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4359b-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="4359b-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4359b-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4359b-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4359b-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4359b-2523">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4359b-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4359b-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4359b-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4359b-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4359b-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4359b-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4359b-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4359b-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4359b-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="4359b-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4359b-2530">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4359b-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4359b-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4359b-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4359b-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4359b-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4359b-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4359b-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4359b-2534">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4359b-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4359b-2535">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4359b-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="4359b-2537">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4359b-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4359b-2538">Az.Profile</span></span>
- <span data-ttu-id="4359b-2539">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4359b-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="4359b-2541">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4359b-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2542">Az.Resources</span></span>
- <span data-ttu-id="4359b-2543">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4359b-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="4359b-2545">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="4359b-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4359b-2546">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4359b-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4359b-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="4359b-2548">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4359b-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4359b-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2549">Az.Sql</span></span>
- <span data-ttu-id="4359b-2550">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="4359b-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4359b-2551">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="4359b-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4359b-2552">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4359b-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2553">Az.Storage</span></span>
- <span data-ttu-id="4359b-2554">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4359b-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2555">Az.Websites</span></span>
- <span data-ttu-id="4359b-2556">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4359b-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4359b-2557">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4359b-2558">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-2558">General</span></span>

* <span data-ttu-id="4359b-2559">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4359b-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4359b-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2560">Az.Compute</span></span>

* <span data-ttu-id="4359b-2561">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="4359b-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="4359b-2563">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="4359b-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4359b-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4359b-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="4359b-2565">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="4359b-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="4359b-2566">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4359b-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4359b-2567">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4359b-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4359b-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="4359b-2569">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4359b-2570">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="4359b-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4359b-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2571">Az.Resources</span></span>

* <span data-ttu-id="4359b-2572">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4359b-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4359b-2573">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="4359b-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4359b-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2574">Az.Sql</span></span>

* <span data-ttu-id="4359b-2575">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4359b-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4359b-2576">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="4359b-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4359b-2577">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="4359b-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4359b-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2578">Az.Storage</span></span>

* <span data-ttu-id="4359b-2579">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4359b-2580">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="4359b-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4359b-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4359b-2582">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="4359b-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="4359b-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4359b-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4359b-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4359b-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4359b-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2585">Az.Websites</span></span>

* <span data-ttu-id="4359b-2586">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4359b-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="4359b-2587">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4359b-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4359b-2588">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4359b-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4359b-2589">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4359b-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4359b-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="4359b-2591">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4359b-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4359b-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4359b-2592">Az.Automation</span></span>
* <span data-ttu-id="4359b-2593">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="4359b-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4359b-2594">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4359b-2595">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4359b-2596">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="4359b-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4359b-2597">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="4359b-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4359b-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2598">Az.Compute</span></span>
* <span data-ttu-id="4359b-2599">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4359b-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4359b-2600">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4359b-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4359b-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="4359b-2602">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4359b-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4359b-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4359b-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4359b-2604">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="4359b-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4359b-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2605">Az.Network</span></span>
* <span data-ttu-id="4359b-2606">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4359b-2607">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="4359b-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4359b-2608">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="4359b-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="4359b-2609">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4359b-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4359b-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4359b-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4359b-2611">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="4359b-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4359b-2612">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="4359b-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4359b-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4359b-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4359b-2614">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4359b-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4359b-2615">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4359b-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4359b-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4359b-2616">Az.Relay</span></span>
* <span data-ttu-id="4359b-2617">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4359b-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4359b-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2618">Az.Resources</span></span>
* <span data-ttu-id="4359b-2619">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4359b-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4359b-2620">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="4359b-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4359b-2621">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4359b-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4359b-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-2623">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="4359b-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4359b-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2624">Az.Sql</span></span>
* <span data-ttu-id="4359b-2625">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="4359b-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4359b-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4359b-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4359b-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4359b-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4359b-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4359b-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4359b-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4359b-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4359b-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4359b-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4359b-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4359b-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4359b-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4359b-2634">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4359b-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4359b-2635">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4359b-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4359b-2636">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="4359b-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4359b-2637">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4359b-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4359b-2638">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4359b-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4359b-2639">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4359b-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4359b-2640">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4359b-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4359b-2641">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4359b-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4359b-2642">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4359b-2643">Geral</span><span class="sxs-lookup"><span data-stu-id="4359b-2643">General</span></span>
* <span data-ttu-id="4359b-2644">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="4359b-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4359b-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4359b-2645">Az.Profile</span></span>
* <span data-ttu-id="4359b-2646">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4359b-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4359b-2647">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="4359b-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4359b-2648">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4359b-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4359b-2649">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="4359b-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4359b-2650">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="4359b-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4359b-2651">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4359b-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4359b-2652">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="4359b-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-2654">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4359b-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2655">Az.Compute</span></span>
* <span data-ttu-id="4359b-2656">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4359b-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4359b-2657">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4359b-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4359b-2658">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="4359b-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2660">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4359b-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4359b-2661">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="4359b-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4359b-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4359b-2662">Az.Insights</span></span>
* <span data-ttu-id="4359b-2663">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="4359b-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4359b-2664">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="4359b-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4359b-2665">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="4359b-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4359b-2666">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="4359b-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2667">Az.Network</span></span>
* <span data-ttu-id="4359b-2668">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="4359b-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4359b-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4359b-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4359b-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4359b-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4359b-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4359b-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4359b-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4359b-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4359b-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4359b-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4359b-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4359b-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4359b-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="4359b-2676">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="4359b-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2677">Az.Resources</span></span>
* <span data-ttu-id="4359b-2678">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4359b-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4359b-2679">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="4359b-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4359b-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4359b-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="4359b-2681">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="4359b-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4359b-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4359b-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="4359b-2683">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="4359b-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4359b-2684">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="4359b-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4359b-2685">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4359b-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4359b-2686">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4359b-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4359b-2687">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="4359b-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4359b-2688">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4359b-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4359b-2689">Az.Profile</span></span>
* <span data-ttu-id="4359b-2690">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="4359b-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4359b-2691">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4359b-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2692">Az.Compute</span></span>
* <span data-ttu-id="4359b-2693">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="4359b-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4359b-2694">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4359b-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4359b-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4359b-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="4359b-2696">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4359b-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4359b-2697">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4359b-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4359b-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4359b-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4359b-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4359b-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4359b-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4359b-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2701">Az.Network</span></span>
* <span data-ttu-id="4359b-2702">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="4359b-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4359b-2703">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4359b-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2704">Az.Resources</span></span>
* <span data-ttu-id="4359b-2705">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="4359b-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4359b-2706">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="4359b-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4359b-2707">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4359b-2708">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4359b-2708">Azure.Storage</span></span>
* <span data-ttu-id="4359b-2709">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="4359b-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4359b-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4359b-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4359b-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4359b-2712">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4359b-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4359b-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4359b-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4359b-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4359b-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="4359b-2715">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="4359b-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4359b-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4359b-2716">Az.Compute</span></span>
* <span data-ttu-id="4359b-2717">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="4359b-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4359b-2718">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4359b-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4359b-2719">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="4359b-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4359b-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4359b-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4359b-2721">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4359b-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4359b-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4359b-2722">Az.Network</span></span>
* <span data-ttu-id="4359b-2723">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="4359b-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4359b-2724">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="4359b-2724">new cmdlets added</span></span>
    - <span data-ttu-id="4359b-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4359b-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4359b-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4359b-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4359b-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4359b-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4359b-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4359b-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4359b-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4359b-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4359b-2731">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="4359b-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4359b-2732">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4359b-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4359b-2733">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4359b-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4359b-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4359b-2734">Az.RedisCache</span></span>
* <span data-ttu-id="4359b-2735">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="4359b-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4359b-2736">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4359b-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4359b-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4359b-2737">Az.Resources</span></span>
* <span data-ttu-id="4359b-2738">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4359b-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4359b-2739">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="4359b-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4359b-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4359b-2740">Az.Sql</span></span>
* <span data-ttu-id="4359b-2741">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="4359b-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4359b-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4359b-2742">Az.Websites</span></span>
* <span data-ttu-id="4359b-2743">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="4359b-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4359b-2744">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4359b-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4359b-2745">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4359b-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4359b-2746">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="4359b-2746">Initial Release</span></span>
