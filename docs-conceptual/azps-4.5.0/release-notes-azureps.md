---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 77cbbeb01f5c6fcbf0f61bfab3d3f63b74a53bc4
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566050"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e3217-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e3217-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="e3217-104">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-105">Az.Accounts</span></span>
* <span data-ttu-id="e3217-106">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="e3217-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="e3217-107">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="e3217-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="e3217-108">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="e3217-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="e3217-109">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="e3217-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="e3217-110">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="e3217-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-111">Az.Aks</span></span>
* <span data-ttu-id="e3217-112">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="e3217-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="e3217-113">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="e3217-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-114">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-115">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-116">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-117">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3217-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e3217-118">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="e3217-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="e3217-119">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-120">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3217-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e3217-121">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="e3217-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="e3217-122">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-123">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-124">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3217-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="e3217-125">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="e3217-126">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="e3217-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-128">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e3217-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-129">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-130">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="e3217-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-131">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-132">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="e3217-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="e3217-133">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="e3217-134">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="e3217-135">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="e3217-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="e3217-136">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="e3217-137">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="e3217-138">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-139">Az.Network</span></span>
* <span data-ttu-id="e3217-140">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e3217-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="e3217-141">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="e3217-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="e3217-142">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="e3217-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="e3217-143">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e3217-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-145">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="e3217-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="e3217-146">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3217-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="e3217-147">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3217-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-149">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-150">Az.Resources</span></span>
* <span data-ttu-id="e3217-151">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e3217-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="e3217-152">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="e3217-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-153">Az.Sql</span></span>
* <span data-ttu-id="e3217-154">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="e3217-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="e3217-155">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e3217-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-156">Az.Storage</span></span>
* <span data-ttu-id="e3217-157">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="e3217-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="e3217-158">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="e3217-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="e3217-159">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="e3217-160">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="e3217-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="e3217-161">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="e3217-162">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="e3217-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="e3217-163">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="e3217-164">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-165">Az.Accounts</span></span>
* <span data-ttu-id="e3217-166">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="e3217-167">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="e3217-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-168">Az.Aks</span></span>
* <span data-ttu-id="e3217-169">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="e3217-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="e3217-171">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="e3217-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-172">Az.Automation</span></span>
* <span data-ttu-id="e3217-173">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="e3217-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-174">Az.Compute</span></span>
* <span data-ttu-id="e3217-175">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="e3217-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-176">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-177">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e3217-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e3217-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e3217-178">Az.EventGrid</span></span>
* <span data-ttu-id="e3217-179">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="e3217-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="e3217-180">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-180">Added new features:</span></span>
    - <span data-ttu-id="e3217-181">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="e3217-181">Input mapping</span></span>
    - <span data-ttu-id="e3217-182">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="e3217-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="e3217-183">Link Privado</span><span class="sxs-lookup"><span data-stu-id="e3217-183">Private Link</span></span>
    - <span data-ttu-id="e3217-184">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="e3217-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="e3217-185">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="e3217-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="e3217-186">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="e3217-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="e3217-187">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="e3217-187">WebHook Batching</span></span>
    - <span data-ttu-id="e3217-188">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="e3217-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="e3217-189">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="e3217-189">IpFiltering</span></span>
* <span data-ttu-id="e3217-190">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="e3217-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="e3217-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="e3217-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="e3217-192">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="e3217-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="e3217-193">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="e3217-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="e3217-194">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="e3217-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="e3217-195">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="e3217-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="e3217-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="e3217-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="e3217-197">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="e3217-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="e3217-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="e3217-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="e3217-199">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="e3217-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-200">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-201">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="e3217-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="e3217-202">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="e3217-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-203">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-204">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="e3217-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-205">Az.Monitor</span></span>
* <span data-ttu-id="e3217-206">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="e3217-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-207">Az.Network</span></span>
* <span data-ttu-id="e3217-208">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="e3217-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="e3217-209">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="e3217-210">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e3217-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e3217-211">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e3217-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e3217-212">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e3217-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e3217-213">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="e3217-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="e3217-214">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="e3217-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="e3217-215">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="e3217-216">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e3217-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e3217-217">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e3217-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e3217-218">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e3217-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e3217-219">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="e3217-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="e3217-220">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="e3217-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="e3217-221">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="e3217-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="e3217-222">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="e3217-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="e3217-223">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="e3217-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="e3217-224">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="e3217-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-226">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="e3217-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="e3217-227">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="e3217-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="e3217-228">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="e3217-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-229">Az.Resources</span></span>
* <span data-ttu-id="e3217-230">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="e3217-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="e3217-231">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-232">Az.Sql</span></span>
* <span data-ttu-id="e3217-233">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="e3217-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="e3217-234">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="e3217-235">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="e3217-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-236">Az.Storage</span></span>
* <span data-ttu-id="e3217-237">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="e3217-238">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="e3217-239">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="e3217-240">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-241">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="e3217-242">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="e3217-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="e3217-243">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="e3217-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="e3217-244">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e3217-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="e3217-245">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="e3217-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="e3217-246">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e3217-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="e3217-247">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e3217-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="e3217-248">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="e3217-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="e3217-249">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="e3217-250">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="e3217-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="e3217-251">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="e3217-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="e3217-252">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="e3217-253">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="e3217-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e3217-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e3217-254">Az.StorageSync</span></span>
* <span data-ttu-id="e3217-255">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="e3217-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="e3217-256">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="e3217-257">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="e3217-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="e3217-258">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e3217-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-259">Az.Websites</span></span>
* <span data-ttu-id="e3217-260">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="e3217-261">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-262">Az.Accounts</span></span>
* <span data-ttu-id="e3217-263">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="e3217-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="e3217-264">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="e3217-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="e3217-265">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="e3217-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="e3217-266">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="e3217-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-267">Az.Aks</span></span>
* <span data-ttu-id="e3217-268">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="e3217-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-269">Az.Batch</span></span>
* <span data-ttu-id="e3217-270">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="e3217-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="e3217-271">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-273">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="e3217-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="e3217-274">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="e3217-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-275">Az.Compute</span></span>
* <span data-ttu-id="e3217-276">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e3217-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="e3217-277">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e3217-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="e3217-278">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="e3217-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="e3217-279">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e3217-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="e3217-280">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="e3217-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-281">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-282">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="e3217-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-283">Az.EventHub</span></span>
* <span data-ttu-id="e3217-284">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="e3217-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e3217-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e3217-285">Az.Functions</span></span>
* <span data-ttu-id="e3217-286">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="e3217-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-287">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-288">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3217-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e3217-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e3217-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="e3217-290">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="e3217-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="e3217-291">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="e3217-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-292">Az.Monitor</span></span>
* <span data-ttu-id="e3217-293">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="e3217-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="e3217-294">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="e3217-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-295">Az.Network</span></span>
* <span data-ttu-id="e3217-296">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="e3217-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="e3217-297">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="e3217-298">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="e3217-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="e3217-299">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="e3217-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="e3217-300">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="e3217-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="e3217-301">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="e3217-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="e3217-302">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e3217-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e3217-303">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e3217-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e3217-304">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e3217-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="e3217-305">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="e3217-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="e3217-306">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="e3217-307">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="e3217-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="e3217-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="e3217-309">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="e3217-310">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="e3217-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="e3217-311">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="e3217-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="e3217-312">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="e3217-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="e3217-313">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="e3217-314">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="e3217-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="e3217-315">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="e3217-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="e3217-316">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="e3217-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="e3217-317">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="e3217-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="e3217-318">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="e3217-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="e3217-319">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="e3217-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="e3217-320">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e3217-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="e3217-321">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e3217-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="e3217-322">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="e3217-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="e3217-323">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="e3217-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e3217-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e3217-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e3217-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e3217-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="e3217-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="e3217-330">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e3217-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="e3217-331">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="e3217-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="e3217-332">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e3217-333">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e3217-334">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="e3217-335">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="e3217-336">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e3217-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="e3217-337">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="e3217-338">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="e3217-339">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e3217-340">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e3217-341">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="e3217-342">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="e3217-343">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="e3217-344">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-346">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="e3217-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="e3217-347">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e3217-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="e3217-348">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="e3217-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="e3217-349">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e3217-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="e3217-350">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e3217-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-352">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="e3217-353">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="e3217-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-354">Az.Resources</span></span>
* <span data-ttu-id="e3217-355">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="e3217-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="e3217-356">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="e3217-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="e3217-357">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e3217-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="e3217-358">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="e3217-359">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="e3217-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="e3217-360">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="e3217-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-361">Az.Sql</span></span>
* <span data-ttu-id="e3217-362">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="e3217-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="e3217-363">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="e3217-364">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="e3217-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-365">Az.Storage</span></span>
* <span data-ttu-id="e3217-366">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="e3217-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="e3217-367">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-368">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-369">Az.Websites</span></span>
* <span data-ttu-id="e3217-370">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="e3217-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e3217-371">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="e3217-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="e3217-372">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="e3217-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="e3217-373">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3217-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="e3217-374">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="e3217-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="e3217-375">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="e3217-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="e3217-376">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-377">Az.Accounts</span></span>
* <span data-ttu-id="e3217-378">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="e3217-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="e3217-380">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-381">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-382">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="e3217-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e3217-383">Az.Billing</span></span>
* <span data-ttu-id="e3217-384">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-386">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="e3217-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-387">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-388">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="e3217-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="e3217-389">Az.DataShare</span></span>
* <span data-ttu-id="e3217-390">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="e3217-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="e3217-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="e3217-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="e3217-392">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="e3217-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-394">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="e3217-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="e3217-395">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="e3217-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="e3217-396">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e3217-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="e3217-397">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e3217-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-399">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="e3217-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e3217-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e3217-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e3217-401">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e3217-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e3217-402">Az.PrivateDns</span></span>
* <span data-ttu-id="e3217-403">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e3217-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-405">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="e3217-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="e3217-406">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e3217-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-407">Az.Resources</span></span>
* <span data-ttu-id="e3217-408">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="e3217-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="e3217-409">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="e3217-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="e3217-410">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="e3217-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="e3217-411">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3217-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="e3217-412">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-413">Az.Sql</span></span>
* <span data-ttu-id="e3217-414">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e3217-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e3217-415">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e3217-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e3217-416">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="e3217-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-417">Az.Storage</span></span>
* <span data-ttu-id="e3217-418">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="e3217-419">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e3217-420">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="e3217-420">Highlights since the last release</span></span>
* <span data-ttu-id="e3217-421">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e3217-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="e3217-422">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e3217-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="e3217-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-424">Az.Accounts</span></span>
* <span data-ttu-id="e3217-425">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="e3217-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="e3217-426">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="e3217-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-427">Az.Aks</span></span>
* <span data-ttu-id="e3217-428">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="e3217-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="e3217-429">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="e3217-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="e3217-430">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="e3217-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-431">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-432">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="e3217-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="e3217-433">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="e3217-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="e3217-434">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e3217-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e3217-435">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e3217-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e3217-436">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e3217-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e3217-437">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e3217-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="e3217-438">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e3217-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e3217-439">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e3217-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e3217-440">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e3217-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e3217-441">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e3217-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e3217-442">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="e3217-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="e3217-443">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="e3217-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="e3217-444">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="e3217-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="e3217-445">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3217-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="e3217-446">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="e3217-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="e3217-447">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="e3217-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e3217-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e3217-449">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="e3217-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="e3217-450">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="e3217-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="e3217-451">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="e3217-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-452">Az.Batch</span></span>
* <span data-ttu-id="e3217-453">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="e3217-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="e3217-454">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="e3217-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="e3217-455">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="e3217-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="e3217-456">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="e3217-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="e3217-457">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="e3217-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="e3217-458">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="e3217-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="e3217-459">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="e3217-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="e3217-460">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="e3217-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="e3217-461">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="e3217-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-462">Az.Compute</span></span>
* <span data-ttu-id="e3217-463">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="e3217-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="e3217-464">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="e3217-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="e3217-465">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e3217-465">Breaking changes</span></span>
    - <span data-ttu-id="e3217-466">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="e3217-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="e3217-467">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="e3217-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="e3217-468">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="e3217-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="e3217-469">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="e3217-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="e3217-470">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3217-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="e3217-471">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="e3217-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="e3217-472">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="e3217-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-473">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-474">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e3217-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-475">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-476">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="e3217-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e3217-477">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="e3217-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e3217-478">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="e3217-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="e3217-479">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="e3217-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e3217-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e3217-480">Az.Functions</span></span>
* <span data-ttu-id="e3217-481">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="e3217-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-482">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-483">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="e3217-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e3217-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e3217-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="e3217-485">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="e3217-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-486">Az.IotHub</span></span>
* <span data-ttu-id="e3217-487">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="e3217-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="e3217-488">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="e3217-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="e3217-489">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="e3217-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="e3217-490">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="e3217-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="e3217-491">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="e3217-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="e3217-492">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-492">New cmdlets are:</span></span>
    - <span data-ttu-id="e3217-493">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e3217-494">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e3217-495">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e3217-496">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="e3217-497">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="e3217-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="e3217-498">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="e3217-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-499">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-500">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="e3217-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="e3217-501">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="e3217-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="e3217-502">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="e3217-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="e3217-503">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="e3217-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="e3217-504">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="e3217-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="e3217-505">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="e3217-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="e3217-506">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="e3217-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-507">Az.Monitor</span></span>
* <span data-ttu-id="e3217-508">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="e3217-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="e3217-509">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="e3217-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="e3217-510">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="e3217-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="e3217-511">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="e3217-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="e3217-512">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="e3217-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="e3217-513">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="e3217-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="e3217-514">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="e3217-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-515">Az.Network</span></span>
* <span data-ttu-id="e3217-516">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="e3217-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="e3217-517">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="e3217-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="e3217-518">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="e3217-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="e3217-519">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="e3217-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="e3217-520">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3217-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="e3217-521">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-521">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3217-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e3217-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3217-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e3217-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3217-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e3217-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e3217-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="e3217-526">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="e3217-527">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e3217-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="e3217-528">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="e3217-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="e3217-529">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e3217-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="e3217-530">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e3217-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="e3217-531">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e3217-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="e3217-532">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="e3217-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="e3217-533">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e3217-534">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e3217-535">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e3217-536">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="e3217-537">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e3217-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="e3217-538">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e3217-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="e3217-539">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="e3217-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e3217-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-542">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="e3217-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="e3217-543">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="e3217-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="e3217-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e3217-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="e3217-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e3217-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="e3217-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="e3217-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="e3217-547">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e3217-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="e3217-548">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="e3217-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="e3217-549">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="e3217-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-551">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="e3217-552">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="e3217-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="e3217-553">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="e3217-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="e3217-554">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="e3217-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="e3217-555">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e3217-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-556">Az.Resources</span></span>
* <span data-ttu-id="e3217-557">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="e3217-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="e3217-558">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="e3217-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="e3217-559">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="e3217-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="e3217-560">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="e3217-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="e3217-561">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e3217-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="e3217-562">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e3217-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="e3217-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="e3217-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="e3217-564">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="e3217-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="e3217-565">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="e3217-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="e3217-566">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="e3217-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="e3217-567">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="e3217-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="e3217-568">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="e3217-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="e3217-569">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="e3217-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="e3217-570">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="e3217-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="e3217-571">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="e3217-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="e3217-572">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="e3217-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="e3217-573">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="e3217-574">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="e3217-575">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e3217-576">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-578">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="e3217-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-579">Az.Sql</span></span>
* <span data-ttu-id="e3217-580">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="e3217-580">Enhance performance of:</span></span>
    - <span data-ttu-id="e3217-581">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e3217-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e3217-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e3217-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e3217-583">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e3217-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e3217-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e3217-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e3217-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e3217-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e3217-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e3217-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e3217-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e3217-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e3217-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e3217-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="e3217-589">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="e3217-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="e3217-590">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="e3217-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-591">Az.Storage</span></span>
* <span data-ttu-id="e3217-592">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-593">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="e3217-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="e3217-594">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-595">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="e3217-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="e3217-596">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e3217-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e3217-597">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="e3217-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="e3217-598">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="e3217-599">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="e3217-600">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="e3217-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="e3217-601">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="e3217-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="e3217-602">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="e3217-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="e3217-603">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="e3217-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="e3217-604">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e3217-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="e3217-605">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="e3217-606">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="e3217-607">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-608">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="e3217-609">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e3217-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="e3217-610">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e3217-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e3217-611">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="e3217-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="e3217-612">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="e3217-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="e3217-613">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="e3217-614">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="e3217-615">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="e3217-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="e3217-616">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e3217-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e3217-617">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e3217-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="e3217-618">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e3217-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="e3217-619">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e3217-620">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e3217-621">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="e3217-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="e3217-622">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e3217-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e3217-623">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e3217-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="e3217-624">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e3217-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e3217-625">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e3217-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e3217-626">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e3217-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="e3217-627">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e3217-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="e3217-628">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e3217-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="e3217-629">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e3217-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="e3217-630">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="e3217-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e3217-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e3217-631">Az.TrafficManager</span></span>
* <span data-ttu-id="e3217-632">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="e3217-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-633">Az.Websites</span></span>
* <span data-ttu-id="e3217-634">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="e3217-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="e3217-635">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e3217-636">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="e3217-636">Highlights since the last release</span></span>
* <span data-ttu-id="e3217-637">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e3217-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-638">Az.Accounts</span></span>
* <span data-ttu-id="e3217-639">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="e3217-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-640">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-641">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e3217-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e3217-642">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="e3217-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-643">Az.Cdn</span></span>
* <span data-ttu-id="e3217-644">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="e3217-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-646">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="e3217-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-647">Az.Compute</span></span>
* <span data-ttu-id="e3217-648">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="e3217-649">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="e3217-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-650">Az.IotHub</span></span>
* <span data-ttu-id="e3217-651">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e3217-652">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e3217-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="e3217-653">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e3217-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="e3217-654">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="e3217-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="e3217-655">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e3217-656">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e3217-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="e3217-657">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e3217-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="e3217-658">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="e3217-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="e3217-659">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-659">New cmdlets are:</span></span>
    - <span data-ttu-id="e3217-660">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e3217-661">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e3217-662">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e3217-663">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="e3217-664">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="e3217-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-665">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-666">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="e3217-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="e3217-667">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="e3217-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="e3217-668">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="e3217-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="e3217-669">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e3217-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="e3217-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="e3217-670">Az.Maintenance</span></span>
* <span data-ttu-id="e3217-671">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="e3217-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-672">Az.Monitor</span></span>
* <span data-ttu-id="e3217-673">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="e3217-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="e3217-674">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e3217-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e3217-675">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e3217-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e3217-676">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e3217-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e3217-677">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e3217-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e3217-678">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e3217-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e3217-679">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e3217-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e3217-680">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e3217-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-681">Az.Network</span></span>
* <span data-ttu-id="e3217-682">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="e3217-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="e3217-683">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e3217-684">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e3217-685">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="e3217-686">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="e3217-687">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="e3217-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="e3217-688">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="e3217-689">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="e3217-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="e3217-690">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="e3217-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="e3217-691">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e3217-692">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="e3217-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="e3217-693">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="e3217-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e3217-694">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="e3217-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="e3217-695">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="e3217-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="e3217-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="e3217-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-699">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="e3217-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="e3217-700">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="e3217-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-702">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="e3217-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-703">Az.Sql</span></span>
* <span data-ttu-id="e3217-704">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="e3217-705">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="e3217-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-706">Az.Storage</span></span>
* <span data-ttu-id="e3217-707">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e3217-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e3217-708">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="e3217-709">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="e3217-710">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e3217-711">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="e3217-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="e3217-712">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e3217-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e3217-713">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e3217-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e3217-714">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e3217-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="e3217-715">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e3217-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e3217-716">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="e3217-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="e3217-717">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e3217-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e3217-718">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="e3217-719">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e3217-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="e3217-720">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="e3217-721">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-721">General</span></span>
* <span data-ttu-id="e3217-722">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="e3217-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="e3217-723">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="e3217-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="e3217-724">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="e3217-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="e3217-725">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="e3217-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="e3217-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e3217-726">Az.Billing</span></span>
  - <span data-ttu-id="e3217-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-727">Az.Compute</span></span>
  - <span data-ttu-id="e3217-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e3217-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="e3217-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-729">Az.EventHub</span></span>
  - <span data-ttu-id="e3217-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-730">Az.IotHub</span></span>
  - <span data-ttu-id="e3217-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-731">Az.KeyVault</span></span>
  - <span data-ttu-id="e3217-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-732">Az.Monitor</span></span>
  - <span data-ttu-id="e3217-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-733">Az.Network</span></span>
  - <span data-ttu-id="e3217-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-734">Az.Resources</span></span>
  - <span data-ttu-id="e3217-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-735">Az.Storage</span></span>
  - <span data-ttu-id="e3217-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-736">Az.Websites</span></span>
* <span data-ttu-id="e3217-737">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="e3217-738">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e3217-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="e3217-739">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="e3217-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="e3217-740">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-741">Az.Accounts</span></span>
* <span data-ttu-id="e3217-742">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="e3217-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-743">Az.Compute</span></span>
* <span data-ttu-id="e3217-744">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="e3217-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="e3217-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="e3217-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="e3217-746">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="e3217-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="e3217-747">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="e3217-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="e3217-748">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="e3217-748">[#11354]</span></span>
* <span data-ttu-id="e3217-749">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="e3217-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="e3217-750">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e3217-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e3217-751">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e3217-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e3217-752">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e3217-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e3217-753">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e3217-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="e3217-754">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="e3217-755">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="e3217-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="e3217-756">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e3217-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="e3217-757">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="e3217-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-758">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-759">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="e3217-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="e3217-760">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="e3217-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-762">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="e3217-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="e3217-763">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="e3217-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-764">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-765">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="e3217-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-766">Az.IotHub</span></span>
* <span data-ttu-id="e3217-767">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3217-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="e3217-768">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="e3217-769">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e3217-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="e3217-770">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e3217-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-771">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-772">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="e3217-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-773">Az.Monitor</span></span>
* <span data-ttu-id="e3217-774">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="e3217-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-775">Az.Network</span></span>
* <span data-ttu-id="e3217-776">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="e3217-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="e3217-777">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e3217-778">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e3217-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e3217-779">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e3217-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="e3217-780">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e3217-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="e3217-781">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="e3217-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-783">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="e3217-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-785">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="e3217-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="e3217-786">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="e3217-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="e3217-787">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="e3217-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="e3217-788">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="e3217-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="e3217-789">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e3217-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="e3217-790">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="e3217-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-791">Az.Resources</span></span>
* <span data-ttu-id="e3217-792">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="e3217-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="e3217-793">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="e3217-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="e3217-794">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="e3217-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="e3217-795">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-795">Added example.</span></span>
* <span data-ttu-id="e3217-796">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="e3217-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="e3217-797">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="e3217-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-798">Az.Sql</span></span>
* <span data-ttu-id="e3217-799">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="e3217-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="e3217-800">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e3217-801">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="e3217-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="e3217-802">Az.Support</span></span>
* <span data-ttu-id="e3217-803">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="e3217-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-804">Az.Websites</span></span>
* <span data-ttu-id="e3217-805">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="e3217-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="e3217-806">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e3217-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e3217-807">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e3217-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e3217-808">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e3217-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e3217-809">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e3217-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="e3217-810">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-811">Az.Accounts</span></span>
* <span data-ttu-id="e3217-812">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="e3217-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="e3217-813">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="e3217-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="e3217-814">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="e3217-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-815">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-816">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="e3217-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="e3217-817">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="e3217-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="e3217-818">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="e3217-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="e3217-819">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="e3217-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-821">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="e3217-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-822">Az.IotHub</span></span>
* <span data-ttu-id="e3217-823">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e3217-824">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="e3217-825">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-826">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-827">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-828">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="e3217-829">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="e3217-830">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="e3217-831">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e3217-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="e3217-832">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e3217-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="e3217-833">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e3217-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="e3217-834">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e3217-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="e3217-835">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e3217-836">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e3217-837">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="e3217-838">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="e3217-839">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e3217-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="e3217-840">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e3217-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="e3217-841">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3217-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-842">Az.Monitor</span></span>
* <span data-ttu-id="e3217-843">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="e3217-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-844">Az.Network</span></span>
* <span data-ttu-id="e3217-845">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="e3217-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="e3217-846">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="e3217-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="e3217-847">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="e3217-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="e3217-848">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e3217-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-849">Az.Resources</span></span>
* <span data-ttu-id="e3217-850">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="e3217-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="e3217-851">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="e3217-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="e3217-852">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="e3217-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="e3217-853">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="e3217-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="e3217-854">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="e3217-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="e3217-855">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="e3217-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="e3217-856">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="e3217-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="e3217-857">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="e3217-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e3217-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e3217-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="e3217-861">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="e3217-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="e3217-863">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="e3217-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-864">Az.Sql</span></span>
* <span data-ttu-id="e3217-865">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e3217-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="e3217-866">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e3217-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="e3217-867">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e3217-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="e3217-868">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="e3217-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="e3217-869">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="e3217-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="e3217-870">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e3217-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="e3217-871">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e3217-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="e3217-872">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="e3217-873">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-874">Az.Storage</span></span>
* <span data-ttu-id="e3217-875">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="e3217-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="e3217-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="e3217-877">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e3217-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="e3217-878">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="e3217-879">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e3217-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-880">Az.Websites</span></span>
* <span data-ttu-id="e3217-881">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="e3217-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="e3217-882">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="e3217-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="e3217-883">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="e3217-884">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="e3217-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="e3217-885">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e3217-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="e3217-886">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-887">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-887">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-888">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="e3217-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="e3217-889">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3217-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="e3217-890">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e3217-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-891">Az.Accounts</span></span>
* <span data-ttu-id="e3217-892">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="e3217-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-893">Az.Automation</span></span>
* <span data-ttu-id="e3217-894">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e3217-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-896">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="e3217-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="e3217-897">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="e3217-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-898">Az.Compute</span></span>
* <span data-ttu-id="e3217-899">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="e3217-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-900">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-901">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="e3217-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-902">Az.IotHub</span></span>
* <span data-ttu-id="e3217-903">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e3217-904">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="e3217-905">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-906">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-907">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e3217-908">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e3217-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-909">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-910">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="e3217-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-911">Az.Monitor</span></span>
* <span data-ttu-id="e3217-912">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="e3217-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="e3217-913">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="e3217-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="e3217-914">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="e3217-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-915">Az.Network</span></span>
* <span data-ttu-id="e3217-916">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="e3217-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="e3217-917">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="e3217-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e3217-918">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="e3217-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e3217-919">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="e3217-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="e3217-920">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-920">No new cmdlets are added.</span></span> <span data-ttu-id="e3217-921">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="e3217-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-923">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e3217-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-924">Az.Resources</span></span>
* <span data-ttu-id="e3217-925">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="e3217-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="e3217-926">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3217-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="e3217-927">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e3217-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="e3217-928">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="e3217-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="e3217-929">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e3217-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="e3217-930">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="e3217-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="e3217-931">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="e3217-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="e3217-932">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-933">Az.Sql</span></span>
* <span data-ttu-id="e3217-934">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e3217-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="e3217-935">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="e3217-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="e3217-936">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e3217-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e3217-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e3217-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e3217-938">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="e3217-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e3217-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e3217-939">Az.StorageSync</span></span>
* <span data-ttu-id="e3217-940">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="e3217-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="e3217-941">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-942">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-942">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-943">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e3217-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="e3217-944">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-945">Az.Accounts</span></span>
* <span data-ttu-id="e3217-946">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="e3217-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="e3217-947">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="e3217-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-948">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-949">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="e3217-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="e3217-950">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="e3217-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="e3217-951">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="e3217-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="e3217-952">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="e3217-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-953">Az.Compute</span></span>
* <span data-ttu-id="e3217-954">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="e3217-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="e3217-955">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e3217-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="e3217-956">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e3217-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="e3217-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="e3217-958">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="e3217-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-959">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-960">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="e3217-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e3217-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e3217-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="e3217-962">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="e3217-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="e3217-963">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="e3217-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-964">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-965">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="e3217-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-966">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-967">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="e3217-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-968">Az.Network</span></span>
* <span data-ttu-id="e3217-969">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="e3217-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="e3217-970">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e3217-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="e3217-971">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="e3217-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e3217-972">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="e3217-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="e3217-973">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="e3217-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="e3217-974">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="e3217-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="e3217-975">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="e3217-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="e3217-976">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="e3217-977">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-977">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="e3217-979">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="e3217-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e3217-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="e3217-981">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="e3217-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-983">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="e3217-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="e3217-984">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e3217-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="e3217-985">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="e3217-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="e3217-986">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="e3217-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-988">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="e3217-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="e3217-989">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="e3217-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-990">Az.Resources</span></span>
* <span data-ttu-id="e3217-991">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="e3217-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="e3217-992">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="e3217-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-993">Az.Sql</span></span>
<span data-ttu-id="e3217-994">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="e3217-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-995">Az.Storage</span></span>
* <span data-ttu-id="e3217-996">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="e3217-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="e3217-998">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="e3217-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="e3217-999">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1000">Az.Websites</span></span>
* <span data-ttu-id="e3217-1001">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="e3217-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="e3217-1002">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="e3217-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="e3217-1003">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e3217-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1004">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1005">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e3217-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-1006">Az.Cdn</span></span>
* <span data-ttu-id="e3217-1007">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1008">Az.Compute</span></span>
* <span data-ttu-id="e3217-1009">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="e3217-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e3217-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="e3217-1011">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e3217-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e3217-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e3217-1013">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e3217-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e3217-1014">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="e3217-1015">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e3217-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e3217-1016">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="e3217-1017">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e3217-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e3217-1018">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="e3217-1019">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e3217-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e3217-1020">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="e3217-1021">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e3217-1022">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="e3217-1023">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e3217-1024">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="e3217-1025">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e3217-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e3217-1026">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e3217-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="e3217-1027">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="e3217-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="e3217-1028">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e3217-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="e3217-1029">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="e3217-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="e3217-1030">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="e3217-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1031">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1032">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e3217-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="e3217-1033">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="e3217-1034">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="e3217-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e3217-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="e3217-1036">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="e3217-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1037">Az.EventHub</span></span>
* <span data-ttu-id="e3217-1038">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="e3217-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-1039">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-1040">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="e3217-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e3217-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e3217-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="e3217-1042">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="e3217-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="e3217-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="e3217-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="e3217-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="e3217-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="e3217-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e3217-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="e3217-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="e3217-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="e3217-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="e3217-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1050">Az.Network</span></span>
* <span data-ttu-id="e3217-1051">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="e3217-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1053">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="e3217-1054">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e3217-1055">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e3217-1056">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1057">Az.Resources</span></span>
* <span data-ttu-id="e3217-1058">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1059">Az.Sql</span></span>
* <span data-ttu-id="e3217-1060">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="e3217-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="e3217-1061">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="e3217-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e3217-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e3217-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e3217-1063">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="e3217-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1064">Az.Storage</span></span>
* <span data-ttu-id="e3217-1065">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e3217-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="e3217-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="e3217-1067">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="e3217-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="e3217-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="e3217-1069">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="e3217-1070">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-1070">General</span></span>
* <span data-ttu-id="e3217-1071">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="e3217-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1072">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1073">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="e3217-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="e3217-1074">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="e3217-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-1075">Az.Batch</span></span>
* <span data-ttu-id="e3217-1076">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="e3217-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1077">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1078">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-1080">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="e3217-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="e3217-1081">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="e3217-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e3217-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e3217-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="e3217-1083">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="e3217-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-1084">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-1085">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="e3217-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="e3217-1086">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="e3217-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="e3217-1087">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="e3217-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-1088">Az.Monitor</span></span>
* <span data-ttu-id="e3217-1089">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e3217-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="e3217-1090">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="e3217-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="e3217-1091">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="e3217-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1092">Az.Network</span></span>
* <span data-ttu-id="e3217-1093">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="e3217-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1094">Az.Resources</span></span>
* <span data-ttu-id="e3217-1095">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="e3217-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="e3217-1096">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1097">Az.Sql</span></span>
* <span data-ttu-id="e3217-1098">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="e3217-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1099">Az.Storage</span></span>
* <span data-ttu-id="e3217-1100">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="e3217-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="e3217-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="e3217-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="e3217-1103">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="e3217-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="e3217-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="e3217-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="e3217-1105">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e3217-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="e3217-1106">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="e3217-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="e3217-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="e3217-1109">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="e3217-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="e3217-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e3217-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="e3217-1111">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="e3217-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="e3217-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e3217-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="e3217-1113">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-1114">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-1115">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="e3217-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="e3217-1116">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="e3217-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1117">Az.Compute</span></span>
* <span data-ttu-id="e3217-1118">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="e3217-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="e3217-1119">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="e3217-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="e3217-1120">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="e3217-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="e3217-1121">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="e3217-1122">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e3217-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="e3217-1123">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e3217-1124">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e3217-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="e3217-1125">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="e3217-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="e3217-1126">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e3217-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="e3217-1127">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e3217-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="e3217-1128">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e3217-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e3217-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e3217-1130">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e3217-1131">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="e3217-1131">Get the Order</span></span>
* <span data-ttu-id="e3217-1132">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e3217-1133">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="e3217-1133">Create new Order</span></span>
* <span data-ttu-id="e3217-1134">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e3217-1135">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="e3217-1135">Remove the Order</span></span>
* <span data-ttu-id="e3217-1136">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="e3217-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="e3217-1137">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="e3217-1137">Now creates Local Share</span></span>
* <span data-ttu-id="e3217-1138">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="e3217-1139">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e3217-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="e3217-1140">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="e3217-1141">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="e3217-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="e3217-1142">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e3217-1143">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="e3217-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="e3217-1144">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e3217-1145">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="e3217-1145">Create new Triggers</span></span>
* <span data-ttu-id="e3217-1146">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e3217-1147">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="e3217-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1148">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1149">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="e3217-1150">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="e3217-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-1152">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e3217-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1153">Az.EventHub</span></span>
* <span data-ttu-id="e3217-1154">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="e3217-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-1156">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="e3217-1157">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="e3217-1158">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="e3217-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="e3217-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1160">Az.Network</span></span>
* <span data-ttu-id="e3217-1161">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e3217-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e3217-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="e3217-1163">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1165">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="e3217-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="e3217-1166">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e3217-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="e3217-1167">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e3217-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e3217-1168">Az.RedisCache</span></span>
* <span data-ttu-id="e3217-1169">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="e3217-1170">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="e3217-1171">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="e3217-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1172">Az.Resources</span></span>
- <span data-ttu-id="e3217-1173">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="e3217-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="e3217-1174">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="e3217-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="e3217-1175">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="e3217-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="e3217-1176">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3217-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="e3217-1177">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="e3217-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1178">Az.Sql</span></span>
* <span data-ttu-id="e3217-1179">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="e3217-1180">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="e3217-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="e3217-1181">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="e3217-1182">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-1182">General</span></span>
* <span data-ttu-id="e3217-1183">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="e3217-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1184">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1185">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e3217-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e3217-1186">Az.Advisor</span></span>
* <span data-ttu-id="e3217-1187">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3217-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-1188">Az.Batch</span></span>
* <span data-ttu-id="e3217-1189">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="e3217-1190">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="e3217-1191">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="e3217-1192">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="e3217-1193">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="e3217-1194">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="e3217-1195">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="e3217-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="e3217-1196">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="e3217-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="e3217-1197">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="e3217-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="e3217-1198">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e3217-1199">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="e3217-1200">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="e3217-1201">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e3217-1202">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="e3217-1203">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="e3217-1204">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="e3217-1205">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="e3217-1206">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="e3217-1207">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="e3217-1208">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e3217-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="e3217-1209">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e3217-1210">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e3217-1211">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="e3217-1212">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="e3217-1213">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="e3217-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="e3217-1214">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="e3217-1215">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="e3217-1216">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="e3217-1217">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="e3217-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="e3217-1218">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="e3217-1219">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="e3217-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="e3217-1220">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="e3217-1221">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="e3217-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="e3217-1222">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e3217-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="e3217-1223">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="e3217-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="e3217-1224">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="e3217-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-1225">Az.Cdn</span></span>
* <span data-ttu-id="e3217-1226">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="e3217-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="e3217-1227">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="e3217-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1228">Az.Compute</span></span>
* <span data-ttu-id="e3217-1229">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="e3217-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="e3217-1230">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="e3217-1231">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e3217-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="e3217-1232">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e3217-1233">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="e3217-1234">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="e3217-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="e3217-1235">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="e3217-1236">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e3217-1236">Breaking changes</span></span>
    - <span data-ttu-id="e3217-1237">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="e3217-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="e3217-1238">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e3217-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1239">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1240">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-1242">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="e3217-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="e3217-1243">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="e3217-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="e3217-1244">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="e3217-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="e3217-1245">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="e3217-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="e3217-1246">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="e3217-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="e3217-1247">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="e3217-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-1249">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="e3217-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-1250">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-1251">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="e3217-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="e3217-1252">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e3217-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="e3217-1253">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="e3217-1254">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="e3217-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="e3217-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e3217-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e3217-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e3217-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e3217-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e3217-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e3217-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="e3217-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="e3217-1260">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="e3217-1261">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e3217-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e3217-1262">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e3217-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e3217-1263">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e3217-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="e3217-1264">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="e3217-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="e3217-1265">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="e3217-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="e3217-1266">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="e3217-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="e3217-1267">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="e3217-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="e3217-1268">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e3217-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="e3217-1269">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="e3217-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="e3217-1270">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="e3217-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="e3217-1271">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="e3217-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="e3217-1272">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1273">Az.IotHub</span></span>
* <span data-ttu-id="e3217-1274">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="e3217-1274">Breaking changes:</span></span>
    - <span data-ttu-id="e3217-1275">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e3217-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e3217-1276">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e3217-1277">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e3217-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e3217-1278">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e3217-1279">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="e3217-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="e3217-1280">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="e3217-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="e3217-1281">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="e3217-1282">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="e3217-1283">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e3217-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e3217-1284">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e3217-1285">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e3217-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e3217-1286">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1288">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1289">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="e3217-1290">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="e3217-1291">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1292">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1293">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1294">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1295">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-1296">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="e3217-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1297">Az.Resources</span></span>
* <span data-ttu-id="e3217-1298">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="e3217-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1299">Az.Network</span></span>
* <span data-ttu-id="e3217-1300">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="e3217-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="e3217-1301">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="e3217-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e3217-1307">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="e3217-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="e3217-1308">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-1308">New cmdlet:</span></span>
        - <span data-ttu-id="e3217-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e3217-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="e3217-1310">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="e3217-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="e3217-1311">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="e3217-1312">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="e3217-1313">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="e3217-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="e3217-1314">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="e3217-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="e3217-1315">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="e3217-1316">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="e3217-1317">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e3217-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="e3217-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e3217-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e3217-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e3217-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="e3217-1323">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e3217-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="e3217-1324">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e3217-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e3217-1325">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e3217-1326">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e3217-1327">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="e3217-1328">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="e3217-1329">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="e3217-1330">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="e3217-1332">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e3217-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e3217-1333">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e3217-1334">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e3217-1335">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e3217-1336">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e3217-1337">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="e3217-1338">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="e3217-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="e3217-1339">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="e3217-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="e3217-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e3217-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="e3217-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e3217-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="e3217-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e3217-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="e3217-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="e3217-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="e3217-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="e3217-1346">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e3217-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e3217-1347">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="e3217-1348">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="e3217-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="e3217-1349">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="e3217-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="e3217-1350">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="e3217-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="e3217-1351">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e3217-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e3217-1352">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="e3217-1353">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="e3217-1354">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="e3217-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="e3217-1355">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="e3217-1356">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="e3217-1357">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="e3217-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="e3217-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="e3217-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-1363">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="e3217-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1364">Az.Sql</span></span>
* <span data-ttu-id="e3217-1365">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="e3217-1366">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="e3217-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="e3217-1367">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="e3217-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="e3217-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="e3217-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="e3217-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="e3217-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="e3217-1370">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e3217-1371">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="e3217-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="e3217-1372">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="e3217-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="e3217-1373">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1374">Az.Storage</span></span>
* <span data-ttu-id="e3217-1375">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="e3217-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e3217-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e3217-1378">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="e3217-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="e3217-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e3217-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="e3217-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e3217-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="e3217-1381">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e3217-1382">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-1382">General</span></span>
* <span data-ttu-id="e3217-1383">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1384">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1385">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="e3217-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-1387">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e3217-1388">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="e3217-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-1389">Az.Automation</span></span>
* <span data-ttu-id="e3217-1390">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="e3217-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-1391">Az.Batch</span></span>
* <span data-ttu-id="e3217-1392">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="e3217-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1393">Az.Compute</span></span>
* <span data-ttu-id="e3217-1394">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e3217-1395">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e3217-1396">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="e3217-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="e3217-1397">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="e3217-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1398">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1399">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="e3217-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e3217-1400">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="e3217-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e3217-1401">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-1403">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="e3217-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e3217-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e3217-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="e3217-1405">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e3217-1406">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="e3217-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e3217-1407">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="e3217-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e3217-1408">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="e3217-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1409">Az.IotHub</span></span>
* <span data-ttu-id="e3217-1410">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e3217-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e3217-1411">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3217-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-1412">Az.Monitor</span></span>
* <span data-ttu-id="e3217-1413">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e3217-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e3217-1414">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="e3217-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e3217-1415">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="e3217-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e3217-1416">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3217-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1417">Az.Network</span></span>
* <span data-ttu-id="e3217-1418">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="e3217-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e3217-1419">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e3217-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e3217-1420">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e3217-1422">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e3217-1423">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="e3217-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e3217-1424">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="e3217-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e3217-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e3217-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e3217-1428">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="e3217-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e3217-1429">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e3217-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e3217-1430">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e3217-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e3217-1431">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e3217-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e3217-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e3217-1432">Az.RedisCache</span></span>
* <span data-ttu-id="e3217-1433">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="e3217-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1434">Az.Sql</span></span>
* <span data-ttu-id="e3217-1435">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="e3217-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1436">Az.Storage</span></span>
* <span data-ttu-id="e3217-1437">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="e3217-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e3217-1438">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e3217-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e3217-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e3217-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e3217-1440">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e3217-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e3217-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e3217-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e3217-1442">Az.StorageSync</span></span>
* <span data-ttu-id="e3217-1443">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="e3217-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1444">Az.Websites</span></span>
* <span data-ttu-id="e3217-1445">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="e3217-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e3217-1446">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e3217-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-1448">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e3217-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e3217-1449">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="e3217-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e3217-1450">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-1451">Az.Automation</span></span>
* <span data-ttu-id="e3217-1452">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="e3217-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e3217-1453">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="e3217-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e3217-1454">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="e3217-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1455">Az.Compute</span></span>
* <span data-ttu-id="e3217-1456">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e3217-1457">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e3217-1458">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="e3217-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e3217-1459">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e3217-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e3217-1460">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e3217-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e3217-1461">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3217-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e3217-1462">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="e3217-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e3217-1463">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="e3217-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e3217-1464">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e3217-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1465">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1466">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e3217-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e3217-1467">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="e3217-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-1468">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-1469">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="e3217-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1470">Az.IotHub</span></span>
* <span data-ttu-id="e3217-1471">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="e3217-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e3217-1472">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="e3217-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e3217-1473">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e3217-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="e3217-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e3217-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e3217-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e3217-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e3217-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e3217-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e3217-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e3217-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-1478">Az.Monitor</span></span>
* <span data-ttu-id="e3217-1479">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="e3217-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e3217-1480">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="e3217-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e3217-1481">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="e3217-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e3217-1482">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e3217-1483">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="e3217-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e3217-1484">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="e3217-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e3217-1485">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e3217-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e3217-1486">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e3217-1487">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="e3217-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e3217-1488">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="e3217-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e3217-1489">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="e3217-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e3217-1490">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="e3217-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e3217-1491">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="e3217-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e3217-1492">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="e3217-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e3217-1493">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="e3217-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e3217-1494">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="e3217-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e3217-1495">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="e3217-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e3217-1496">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e3217-1497">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="e3217-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e3217-1498">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-1498">Overall improved help files</span></span>
* <span data-ttu-id="e3217-1499">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="e3217-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1500">Az.Network</span></span>
* <span data-ttu-id="e3217-1501">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="e3217-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="e3217-1502">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="e3217-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e3217-1503">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="e3217-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e3217-1504">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="e3217-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e3217-1505">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="e3217-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e3217-1506">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="e3217-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e3217-1507">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="e3217-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e3217-1508">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e3217-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e3217-1509">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e3217-1510">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="e3217-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e3217-1511">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e3217-1512">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="e3217-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e3217-1513">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1513">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e3217-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e3217-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e3217-1516">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="e3217-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e3217-1517">New-VpnSite</span></span>
        - <span data-ttu-id="e3217-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e3217-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="e3217-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="e3217-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="e3217-1521">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="e3217-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1523">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="e3217-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e3217-1524">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="e3217-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1525">Az.Resources</span></span>
* <span data-ttu-id="e3217-1526">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="e3217-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-1528">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="e3217-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e3217-1529">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="e3217-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e3217-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e3217-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e3217-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e3217-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e3217-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e3217-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e3217-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e3217-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e3217-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e3217-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e3217-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e3217-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e3217-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e3217-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e3217-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e3217-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e3217-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e3217-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e3217-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e3217-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e3217-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e3217-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e3217-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e3217-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e3217-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e3217-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e3217-1543">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e3217-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e3217-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e3217-1544">Az.SignalR</span></span>
* <span data-ttu-id="e3217-1545">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="e3217-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1546">Az.Sql</span></span>
* <span data-ttu-id="e3217-1547">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="e3217-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e3217-1548">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="e3217-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e3217-1549">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e3217-1550">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e3217-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e3217-1551">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="e3217-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1552">Az.Storage</span></span>
* <span data-ttu-id="e3217-1553">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e3217-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e3217-1554">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="e3217-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e3217-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e3217-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e3217-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e3217-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e3217-1557">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="e3217-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e3217-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e3217-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e3217-1559">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e3217-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e3217-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e3217-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e3217-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e3217-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e3217-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1564">Az.Websites</span></span>
* <span data-ttu-id="e3217-1565">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="e3217-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e3217-1566">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="e3217-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e3217-1567">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="e3217-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e3217-1568">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e3217-1569">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-1569">General</span></span>
* <span data-ttu-id="e3217-1570">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="e3217-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1571">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1572">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="e3217-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-1573">Az.Aks</span></span>
* <span data-ttu-id="e3217-1574">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="e3217-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e3217-1575">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e3217-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-1577">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="e3217-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e3217-1578">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="e3217-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e3217-1579">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="e3217-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e3217-1580">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e3217-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e3217-1581">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e3217-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-1582">Az.Batch</span></span>
* <span data-ttu-id="e3217-1583">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="e3217-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-1584">Az.Cdn</span></span>
* <span data-ttu-id="e3217-1585">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="e3217-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1586">Az.Compute</span></span>
* <span data-ttu-id="e3217-1587">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e3217-1588">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e3217-1589">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="e3217-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e3217-1590">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e3217-1591">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e3217-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e3217-1592">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e3217-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e3217-1593">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="e3217-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e3217-1594">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="e3217-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1595">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1596">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="e3217-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e3217-1597">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="e3217-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e3217-1598">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="e3217-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e3217-1599">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="e3217-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-1601">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="e3217-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1602">Az.EventHub</span></span>
* <span data-ttu-id="e3217-1603">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e3217-1604">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="e3217-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e3217-1605">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e3217-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e3217-1606">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="e3217-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e3217-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e3217-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e3217-1608">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="e3217-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-1609">Az.Monitor</span></span>
* <span data-ttu-id="e3217-1610">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1611">Az.Network</span></span>
* <span data-ttu-id="e3217-1612">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e3217-1613">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="e3217-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e3217-1614">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="e3217-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e3217-1615">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="e3217-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e3217-1616">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e3217-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="e3217-1617">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e3217-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e3217-1618">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e3217-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-1620">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="e3217-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e3217-1621">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="e3217-1621">Added example</span></span>
    - <span data-ttu-id="e3217-1622">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="e3217-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e3217-1623">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e3217-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e3217-1624">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e3217-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1626">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1627">Az.Resources</span></span>
* <span data-ttu-id="e3217-1628">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="e3217-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e3217-1629">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="e3217-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e3217-1630">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="e3217-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e3217-1631">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-1633">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e3217-1634">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="e3217-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e3217-1635">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="e3217-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-1637">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="e3217-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e3217-1638">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e3217-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e3217-1639">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e3217-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e3217-1640">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="e3217-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e3217-1641">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e3217-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e3217-1642">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e3217-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1643">Az.Sql</span></span>
* <span data-ttu-id="e3217-1644">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="e3217-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1645">Az.Storage</span></span>
* <span data-ttu-id="e3217-1646">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3217-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e3217-1647">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="e3217-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e3217-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e3217-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e3217-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e3217-1650">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="e3217-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e3217-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1652">Az.Websites</span></span>
* <span data-ttu-id="e3217-1653">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3217-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e3217-1654">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1655">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1656">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e3217-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e3217-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e3217-1658">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="e3217-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-1659">Az.Automation</span></span>
* <span data-ttu-id="e3217-1660">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="e3217-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-1662">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="e3217-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1663">Az.Compute</span></span>
* <span data-ttu-id="e3217-1664">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="e3217-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e3217-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e3217-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e3217-1666">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="e3217-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e3217-1667">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e3217-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1668">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1669">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e3217-1670">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="e3217-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1671">Az.EventHub</span></span>
* <span data-ttu-id="e3217-1672">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e3217-1673">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="e3217-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-1674">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-1675">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="e3217-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e3217-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e3217-1676">Az.LogicApp</span></span>
* <span data-ttu-id="e3217-1677">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="e3217-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e3217-1678">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="e3217-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e3217-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="e3217-1680">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="e3217-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1681">Az.Network</span></span>
* <span data-ttu-id="e3217-1682">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="e3217-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e3217-1683">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1683">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e3217-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e3217-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e3217-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e3217-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e3217-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e3217-1692">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="e3217-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e3217-1693">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="e3217-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e3217-1694">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e3217-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e3217-1695">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e3217-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e3217-1696">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="e3217-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e3217-1697">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="e3217-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e3217-1698">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="e3217-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="e3217-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e3217-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e3217-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e3217-1702">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e3217-1703">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e3217-1704">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="e3217-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e3217-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e3217-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e3217-1708">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="e3217-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e3217-1709">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="e3217-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e3217-1710">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="e3217-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-1712">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="e3217-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="e3217-1713">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="e3217-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1715">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e3217-1716">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e3217-1717">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e3217-1718">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e3217-1719">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e3217-1720">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e3217-1721">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e3217-1722">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e3217-1723">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e3217-1724">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="e3217-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1725">Az.Resources</span></span>
- <span data-ttu-id="e3217-1726">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e3217-1727">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e3217-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-1729">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e3217-1730">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="e3217-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1731">Az.Sql</span></span>
* <span data-ttu-id="e3217-1732">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e3217-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e3217-1733">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="e3217-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e3217-1734">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="e3217-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1735">Az.Storage</span></span>
* <span data-ttu-id="e3217-1736">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="e3217-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e3217-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e3217-1737">Az.StorageSync</span></span>
* <span data-ttu-id="e3217-1738">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="e3217-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e3217-1739">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e3217-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1740">Az.Websites</span></span>
* <span data-ttu-id="e3217-1741">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3217-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e3217-1742">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e3217-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e3217-1743">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e3217-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e3217-1744">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1745">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1746">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="e3217-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e3217-1747">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="e3217-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e3217-1748">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e3217-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e3217-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e3217-1749">Az.Advisor</span></span>
* <span data-ttu-id="e3217-1750">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e3217-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e3217-1751">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="e3217-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e3217-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-1753">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e3217-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e3217-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e3217-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e3217-1755">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="e3217-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e3217-1756">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="e3217-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e3217-1757">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e3217-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e3217-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e3217-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e3217-1759">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="e3217-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-1760">Az.Automation</span></span>
* <span data-ttu-id="e3217-1761">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e3217-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1762">Az.Compute</span></span>
* <span data-ttu-id="e3217-1763">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-1764">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-1765">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="e3217-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e3217-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e3217-1766">Az.EventGrid</span></span>
* <span data-ttu-id="e3217-1767">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="e3217-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1768">Az.IotHub</span></span>
* <span data-ttu-id="e3217-1769">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="e3217-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1770">Az.Network</span></span>
* <span data-ttu-id="e3217-1771">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="e3217-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e3217-1772">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="e3217-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-1774">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e3217-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e3217-1775">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e3217-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-1777">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e3217-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1779">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="e3217-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1780">Az.Resources</span></span>
    - <span data-ttu-id="e3217-1781">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="e3217-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e3217-1782">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e3217-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e3217-1783">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e3217-1784">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="e3217-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-1786">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e3217-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1787">Az.Sql</span></span>
* <span data-ttu-id="e3217-1788">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="e3217-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e3217-1789">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e3217-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e3217-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e3217-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e3217-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e3217-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e3217-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e3217-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e3217-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e3217-1796">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="e3217-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1797">Az.Storage</span></span>
* <span data-ttu-id="e3217-1798">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e3217-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e3217-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e3217-1800">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="e3217-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e3217-1801">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="e3217-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e3217-1802">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e3217-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e3217-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e3217-1805">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="e3217-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e3217-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e3217-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e3217-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e3217-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e3217-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e3217-1808">Az.StorageSync</span></span>
* <span data-ttu-id="e3217-1809">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="e3217-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e3217-1810">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-1811">Az.Accounts</span></span>
* <span data-ttu-id="e3217-1812">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="e3217-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e3217-1813">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e3217-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e3217-1814">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="e3217-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e3217-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e3217-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e3217-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e3217-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1817">Az.Compute</span></span>
* <span data-ttu-id="e3217-1818">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e3217-1819">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="e3217-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e3217-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e3217-1820">Az.Dns</span></span>
* <span data-ttu-id="e3217-1821">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e3217-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e3217-1822">Az.EventGrid</span></span>
* <span data-ttu-id="e3217-1823">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e3217-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e3217-1824">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e3217-1824">New cmdlets:</span></span>
    - <span data-ttu-id="e3217-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e3217-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e3217-1826">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e3217-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e3217-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e3217-1828">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e3217-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e3217-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e3217-1830">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e3217-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e3217-1832">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e3217-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e3217-1834">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e3217-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e3217-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e3217-1836">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e3217-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e3217-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e3217-1838">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="e3217-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="e3217-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e3217-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e3217-1840">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="e3217-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e3217-1841">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="e3217-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="e3217-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e3217-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e3217-1843">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e3217-1844">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e3217-1845">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="e3217-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e3217-1846">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e3217-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e3217-1847">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="e3217-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e3217-1848">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="e3217-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e3217-1849">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="e3217-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e3217-1850">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="e3217-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="e3217-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e3217-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e3217-1852">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="e3217-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e3217-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e3217-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e3217-1854">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e3217-1855">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e3217-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e3217-1858">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e3217-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e3217-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e3217-1860">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="e3217-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1861">Az.Network</span></span>
* <span data-ttu-id="e3217-1862">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e3217-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e3217-1863">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1863">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e3217-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e3217-1865">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e3217-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e3217-1866">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1866">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e3217-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e3217-1868">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e3217-1869">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1869">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e3217-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e3217-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e3217-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e3217-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e3217-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e3217-1875">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e3217-1876">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-1876">New cmdlets</span></span>
        - <span data-ttu-id="e3217-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e3217-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e3217-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3217-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e3217-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e3217-1881">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e3217-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e3217-1882">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e3217-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e3217-1883">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e3217-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e3217-1884">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e3217-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e3217-1885">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e3217-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e3217-1886">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e3217-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e3217-1887">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e3217-1888">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="e3217-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e3217-1889">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e3217-1890">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="e3217-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e3217-1891">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e3217-1892">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e3217-1893">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e3217-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e3217-1894">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e3217-1895">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="e3217-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e3217-1896">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="e3217-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e3217-1897">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e3217-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e3217-1898">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="e3217-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e3217-1899">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e3217-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="e3217-1900">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e3217-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="e3217-1901">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e3217-1902">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e3217-1903">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-1905">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e3217-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-1906">Az.Resources</span></span>
* <span data-ttu-id="e3217-1907">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="e3217-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e3217-1908">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e3217-1909">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e3217-1910">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="e3217-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-1912">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="e3217-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1913">Az.Sql</span></span>
* <span data-ttu-id="e3217-1914">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e3217-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e3217-1915">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e3217-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e3217-1916">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="e3217-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e3217-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e3217-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e3217-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e3217-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e3217-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e3217-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e3217-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e3217-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-1922">Az.Storage</span></span>
* <span data-ttu-id="e3217-1923">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e3217-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="e3217-1925">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="e3217-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e3217-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1927">Az.Websites</span></span>
* <span data-ttu-id="e3217-1928">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="e3217-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e3217-1929">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e3217-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e3217-1930">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e3217-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-1931">Az.Cdn</span></span>
* <span data-ttu-id="e3217-1932">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="e3217-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-1933">Az.Compute</span></span>
* <span data-ttu-id="e3217-1934">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e3217-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e3217-1935">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e3217-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-1936">Az.EventHub</span></span>
* <span data-ttu-id="e3217-1937">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="e3217-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e3217-1938">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3217-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-1939">Az.Network</span></span>
* <span data-ttu-id="e3217-1940">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="e3217-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e3217-1941">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="e3217-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-1943">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e3217-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-1945">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="e3217-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-1947">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3217-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-1949">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="e3217-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e3217-1950">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e3217-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-1951">Az.Sql</span></span>
* <span data-ttu-id="e3217-1952">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e3217-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e3217-1953">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e3217-1954">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e3217-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e3217-1955">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="e3217-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-1956">Az.Websites</span></span>
* <span data-ttu-id="e3217-1957">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="e3217-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e3217-1958">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e3217-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-1960">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e3217-1961">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e3217-1962">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e3217-1963">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="e3217-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e3217-1964">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e3217-1965">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e3217-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e3217-1966">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e3217-1967">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e3217-1968">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e3217-1969">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="e3217-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e3217-1970">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e3217-1971">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="e3217-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e3217-1972">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="e3217-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e3217-1973">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="e3217-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e3217-1974">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="e3217-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e3217-1975">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="e3217-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e3217-1976">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="e3217-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e3217-1977">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="e3217-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e3217-1978">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="e3217-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="e3217-1979">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="e3217-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e3217-1980">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="e3217-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e3217-1981">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="e3217-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e3217-1982">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="e3217-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e3217-1983">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="e3217-1984">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="e3217-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e3217-1985">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="e3217-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e3217-1986">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="e3217-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e3217-1987">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e3217-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e3217-1988">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e3217-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e3217-1989">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="e3217-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e3217-1990">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="e3217-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="e3217-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e3217-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e3217-1992">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="e3217-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e3217-1993">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e3217-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e3217-1994">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="e3217-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e3217-1995">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="e3217-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e3217-1996">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="e3217-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e3217-1997">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="e3217-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e3217-1998">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="e3217-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e3217-1999">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e3217-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e3217-2000">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e3217-2001">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e3217-2002">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e3217-2003">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="e3217-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e3217-2004">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e3217-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e3217-2005">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e3217-2006">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e3217-2007">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="e3217-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e3217-2008">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e3217-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e3217-2009">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e3217-2010">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="e3217-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e3217-2011">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="e3217-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e3217-2012">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="e3217-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e3217-2013">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e3217-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e3217-2014">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="e3217-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e3217-2015">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="e3217-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e3217-2016">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e3217-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e3217-2017">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e3217-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e3217-2018">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e3217-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e3217-2019">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3217-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e3217-2020">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e3217-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e3217-2021">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e3217-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e3217-2022">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e3217-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e3217-2023">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e3217-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e3217-2024">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="e3217-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e3217-2025">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e3217-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e3217-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e3217-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e3217-2027">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e3217-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e3217-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e3217-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e3217-2029">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e3217-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e3217-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e3217-2031">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e3217-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e3217-2032">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e3217-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e3217-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e3217-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e3217-2034">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e3217-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="e3217-2035">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e3217-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e3217-2036">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e3217-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2037">Az.Automation</span></span>
* <span data-ttu-id="e3217-2038">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="e3217-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e3217-2039">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e3217-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e3217-2040">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e3217-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e3217-2041">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="e3217-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e3217-2042">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e3217-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e3217-2043">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="e3217-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e3217-2044">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="e3217-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2045">Az.Compute</span></span>
* <span data-ttu-id="e3217-2046">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e3217-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e3217-2047">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="e3217-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2049">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-2050">Az.Monitor</span></span>
* <span data-ttu-id="e3217-2051">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2052">Az.Network</span></span>
* <span data-ttu-id="e3217-2053">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="e3217-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e3217-2054">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e3217-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="e3217-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e3217-2056">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e3217-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2057">Az.Resources</span></span>
* <span data-ttu-id="e3217-2058">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="e3217-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2059">Az.Sql</span></span>
* <span data-ttu-id="e3217-2060">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="e3217-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e3217-2061">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2062">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2063">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="e3217-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-2065">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="e3217-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e3217-2066">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="e3217-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2067">Az.Compute</span></span>
* <span data-ttu-id="e3217-2068">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e3217-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e3217-2069">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e3217-2070">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e3217-2071">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e3217-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e3217-2072">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e3217-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e3217-2073">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="e3217-2074">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e3217-2074">Breaking changes</span></span>
    - <span data-ttu-id="e3217-2075">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e3217-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e3217-2076">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e3217-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e3217-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e3217-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="e3217-2078">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e3217-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e3217-2079">Az.Dns</span></span>
* <span data-ttu-id="e3217-2080">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="e3217-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e3217-2081">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="e3217-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e3217-2082">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="e3217-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e3217-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="e3217-2084">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e3217-2085">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="e3217-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e3217-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-2086">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-2087">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e3217-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e3217-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e3217-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e3217-2090">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e3217-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e3217-2091">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="e3217-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e3217-2092">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="e3217-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e3217-2093">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="e3217-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-2094">Az.Monitor</span></span>
* <span data-ttu-id="e3217-2095">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="e3217-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="e3217-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e3217-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e3217-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e3217-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e3217-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e3217-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e3217-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e3217-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e3217-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e3217-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e3217-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e3217-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e3217-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e3217-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e3217-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e3217-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e3217-2107">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="e3217-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e3217-2108">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="e3217-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2109">Az.Network</span></span>
* <span data-ttu-id="e3217-2110">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="e3217-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e3217-2111">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e3217-2111">New cmdlets</span></span>
        - <span data-ttu-id="e3217-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="e3217-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e3217-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e3217-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e3217-2116">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="e3217-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="e3217-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e3217-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e3217-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e3217-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e3217-2119">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="e3217-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e3217-2120">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e3217-2121">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3217-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-2123">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="e3217-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e3217-2124">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="e3217-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e3217-2125">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-2127">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e3217-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e3217-2128">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e3217-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e3217-2129">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e3217-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e3217-2130">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e3217-2131">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e3217-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e3217-2132">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="e3217-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e3217-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e3217-2133">Az.Relay</span></span>
* <span data-ttu-id="e3217-2134">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="e3217-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-2136">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="e3217-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2137">Az.Storage</span></span>
* <span data-ttu-id="e3217-2138">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="e3217-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e3217-2139">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="e3217-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e3217-2140">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="e3217-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e3217-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="e3217-2142">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="e3217-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e3217-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e3217-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e3217-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2146">Az.Websites</span></span>
* <span data-ttu-id="e3217-2147">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e3217-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e3217-2148">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="e3217-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e3217-2149">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-2150">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-2151">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e3217-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="e3217-2152">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e3217-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e3217-2153">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e3217-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e3217-2154">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e3217-2155">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e3217-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e3217-2156">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e3217-2157">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e3217-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2158">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2159">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="e3217-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e3217-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-2160">Az.Batch</span></span>
* <span data-ttu-id="e3217-2161">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-2162">Az.Cdn</span></span>
* <span data-ttu-id="e3217-2163">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-2165">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2166">Az.Compute</span></span>
* <span data-ttu-id="e3217-2167">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="e3217-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e3217-2168">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2169">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e3217-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-2170">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-2171">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e3217-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2173">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e3217-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e3217-2174">Az.EventGrid</span></span>
* <span data-ttu-id="e3217-2175">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="e3217-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2176">Az.EventHub</span></span>
* <span data-ttu-id="e3217-2177">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="e3217-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e3217-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e3217-2178">Az.HDInsight</span></span>
* <span data-ttu-id="e3217-2179">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2180">Az.IotHub</span></span>
* <span data-ttu-id="e3217-2181">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2182">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-2183">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2184">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e3217-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e3217-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e3217-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="e3217-2186">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e3217-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e3217-2187">Az.Media</span></span>
* <span data-ttu-id="e3217-2188">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-2189">Az.Monitor</span></span>
  * <span data-ttu-id="e3217-2190">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="e3217-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e3217-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e3217-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e3217-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e3217-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e3217-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e3217-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e3217-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e3217-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e3217-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e3217-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e3217-2196">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e3217-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2197">Az.Network</span></span>
* <span data-ttu-id="e3217-2198">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2199">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e3217-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e3217-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e3217-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="e3217-2201">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-2203">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e3217-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e3217-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e3217-2205">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-2207">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2208">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e3217-2209">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e3217-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e3217-2210">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="e3217-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e3217-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e3217-2211">Az.RedisCache</span></span>
* <span data-ttu-id="e3217-2212">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2213">Az.Resources</span></span>
* <span data-ttu-id="e3217-2214">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e3217-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2215">Az.Sql</span></span>
* <span data-ttu-id="e3217-2216">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="e3217-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e3217-2217">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2218">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="e3217-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e3217-2219">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="e3217-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e3217-2220">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="e3217-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e3217-2221">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e3217-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e3217-2222">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e3217-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2223">Az.Websites</span></span>
* <span data-ttu-id="e3217-2224">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="e3217-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e3217-2225">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e3217-2226">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="e3217-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e3217-2227">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e3217-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e3217-2228">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-2229">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-2230">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e3217-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="e3217-2231">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e3217-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e3217-2232">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e3217-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e3217-2233">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e3217-2234">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e3217-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e3217-2235">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e3217-2236">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e3217-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e3217-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2237">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2238">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e3217-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="e3217-2240">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="e3217-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e3217-2241">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="e3217-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2242">Az.Automation</span></span>
* <span data-ttu-id="e3217-2243">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="e3217-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e3217-2244">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="e3217-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e3217-2245">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2246">Az.Compute</span></span>
* <span data-ttu-id="e3217-2247">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e3217-2248">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="e3217-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e3217-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="e3217-2250">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="e3217-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-2251">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-2252">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e3217-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e3217-2253">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3217-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2254">Az.Resources</span></span>
* <span data-ttu-id="e3217-2255">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="e3217-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e3217-2256">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e3217-2257">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="e3217-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e3217-2258">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e3217-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e3217-2259">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="e3217-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e3217-2260">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e3217-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2261">Az.Sql</span></span>
* <span data-ttu-id="e3217-2262">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="e3217-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2263">Az.Storage</span></span>
* <span data-ttu-id="e3217-2264">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e3217-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3217-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="e3217-2266">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e3217-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e3217-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e3217-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e3217-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e3217-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e3217-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e3217-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e3217-2271">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="e3217-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e3217-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e3217-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e3217-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e3217-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e3217-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e3217-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e3217-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e3217-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e3217-2276">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e3217-2277">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e3217-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="e3217-2278">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e3217-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="e3217-2279">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e3217-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e3217-2280">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e3217-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e3217-2281">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e3217-2282">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e3217-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e3217-2283">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e3217-2284">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e3217-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2285">Az.Automation</span></span>
* <span data-ttu-id="e3217-2286">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e3217-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e3217-2287">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="e3217-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="e3217-2288">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="e3217-2288">Pre-Post script</span></span>
    * <span data-ttu-id="e3217-2289">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="e3217-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2290">Az.Compute</span></span>
* <span data-ttu-id="e3217-2291">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e3217-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e3217-2292">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e3217-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2293">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-2294">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2295">Az.Network</span></span>
* <span data-ttu-id="e3217-2296">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e3217-2297">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="e3217-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-2299">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="e3217-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e3217-2300">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="e3217-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2301">Az.Resources</span></span>
* <span data-ttu-id="e3217-2302">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3217-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e3217-2303">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="e3217-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2304">Az.Sql</span></span>
* <span data-ttu-id="e3217-2305">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="e3217-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2306">Az.Storage</span></span>
* <span data-ttu-id="e3217-2307">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e3217-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e3217-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e3217-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e3217-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e3217-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e3217-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e3217-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e3217-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2314">Az.Websites</span></span>
* <span data-ttu-id="e3217-2315">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="e3217-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="e3217-2316">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2317">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2318">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="e3217-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e3217-2319">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2320">Az.Automation</span></span>
* <span data-ttu-id="e3217-2321">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e3217-2322">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="e3217-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e3217-2323">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="e3217-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-2324">Az.Cdn</span></span>
* <span data-ttu-id="e3217-2325">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="e3217-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2326">Az.Compute</span></span>
* <span data-ttu-id="e3217-2327">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="e3217-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-2328">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-2329">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e3217-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e3217-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e3217-2330">Az.LogicApp</span></span>
* <span data-ttu-id="e3217-2331">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="e3217-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2332">Az.Network</span></span>
* <span data-ttu-id="e3217-2333">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-2335">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e3217-2336">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="e3217-2336">SDK Update</span></span>
* <span data-ttu-id="e3217-2337">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e3217-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e3217-2338">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e3217-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2339">Az.Resources</span></span>
* <span data-ttu-id="e3217-2340">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="e3217-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e3217-2341">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e3217-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e3217-2342">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e3217-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e3217-2343">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e3217-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e3217-2344">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e3217-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e3217-2345">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e3217-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2346">Az.Sql</span></span>
* <span data-ttu-id="e3217-2347">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="e3217-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e3217-2348">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e3217-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2349">Az.Storage</span></span>
* <span data-ttu-id="e3217-2350">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e3217-2351">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="e3217-2353">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2354">Az.Automation</span></span>
* <span data-ttu-id="e3217-2355">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e3217-2356">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e3217-2357">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-2359">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3217-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2360">Az.Compute</span></span>
* <span data-ttu-id="e3217-2361">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="e3217-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e3217-2362">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="e3217-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e3217-2363">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e3217-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e3217-2364">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="e3217-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2366">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="e3217-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e3217-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2367">Az.EventHub</span></span>
* <span data-ttu-id="e3217-2368">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2369">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-2370">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3217-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e3217-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e3217-2371">Az.LogicApp</span></span>
* <span data-ttu-id="e3217-2372">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="e3217-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e3217-2373">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="e3217-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e3217-2374">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="e3217-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e3217-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3217-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e3217-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3217-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e3217-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3217-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e3217-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3217-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e3217-2379">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="e3217-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e3217-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e3217-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e3217-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e3217-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e3217-2384">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e3217-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e3217-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-2385">Az.Monitor</span></span>
* <span data-ttu-id="e3217-2386">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="e3217-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2387">Az.Network</span></span>
* <span data-ttu-id="e3217-2388">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e3217-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="e3217-2390">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="e3217-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e3217-2391">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="e3217-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="e3217-2392">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="e3217-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2393">Az.Resources</span></span>
* <span data-ttu-id="e3217-2394">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e3217-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e3217-2395">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e3217-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e3217-2396">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e3217-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e3217-2397">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e3217-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2398">Az.Sql</span></span>
* <span data-ttu-id="e3217-2399">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e3217-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e3217-2400">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="e3217-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2401">Az.Websites</span></span>
* <span data-ttu-id="e3217-2402">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e3217-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e3217-2403">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2404">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2405">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e3217-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="e3217-2407">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="e3217-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2408">Az.Compute</span></span>
* <span data-ttu-id="e3217-2409">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="e3217-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e3217-2410">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e3217-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e3217-2411">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e3217-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="e3217-2413">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="e3217-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2414">Az.Resources</span></span>
* <span data-ttu-id="e3217-2415">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="e3217-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="e3217-2416">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e3217-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e3217-2417">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e3217-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="e3217-2418">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e3217-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2419">Az.Sql</span></span>
* <span data-ttu-id="e3217-2420">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e3217-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e3217-2421">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="e3217-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e3217-2422">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e3217-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e3217-2423">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2424">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2425">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="e3217-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e3217-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="e3217-2427">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="e3217-2429">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e3217-2430">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2431">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2432">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e3217-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e3217-2433">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e3217-2434">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e3217-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e3217-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e3217-2435">Az.Aks</span></span>
* <span data-ttu-id="e3217-2436">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e3217-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2437">Az.Automation</span></span>
* <span data-ttu-id="e3217-2438">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="e3217-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e3217-2439">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e3217-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e3217-2440">Az.Cdn</span></span>
* <span data-ttu-id="e3217-2441">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2442">Az.Compute</span></span>
* <span data-ttu-id="e3217-2443">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e3217-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e3217-2444">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e3217-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e3217-2445">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e3217-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e3217-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e3217-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e3217-2447">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e3217-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e3217-2448">Az.DataFactory</span></span>
* <span data-ttu-id="e3217-2449">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e3217-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2451">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="e3217-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e3217-2452">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e3217-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e3217-2453">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2454">Az.IotHub</span></span>
* <span data-ttu-id="e3217-2455">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e3217-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e3217-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2456">Az.KeyVault</span></span>
* <span data-ttu-id="e3217-2457">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2458">Az.Network</span></span>
* <span data-ttu-id="e3217-2459">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2460">Az.Resources</span></span>
* <span data-ttu-id="e3217-2461">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="e3217-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e3217-2462">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e3217-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e3217-2463">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="e3217-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e3217-2464">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e3217-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e3217-2465">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e3217-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e3217-2466">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e3217-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e3217-2467">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e3217-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-2469">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e3217-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e3217-2470">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="e3217-2470">Fix some error messages.</span></span>
* <span data-ttu-id="e3217-2471">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="e3217-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e3217-2472">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="e3217-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e3217-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e3217-2473">Az.SignalR</span></span>
* <span data-ttu-id="e3217-2474">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2475">Az.Sql</span></span>
* <span data-ttu-id="e3217-2476">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e3217-2477">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e3217-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e3217-2478">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="e3217-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e3217-2479">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="e3217-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2480">Az.Storage</span></span>
* <span data-ttu-id="e3217-2481">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e3217-2482">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e3217-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e3217-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e3217-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e3217-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e3217-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e3217-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="e3217-2486">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2487">Az.Websites</span></span>
* <span data-ttu-id="e3217-2488">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e3217-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e3217-2489">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="e3217-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e3217-2490">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e3217-2491">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e3217-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e3217-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2492">Az.Accounts</span></span>
* <span data-ttu-id="e3217-2493">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e3217-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2494">Az.Compute</span></span>
* <span data-ttu-id="e3217-2495">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e3217-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e3217-2496">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e3217-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e3217-2497">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2499">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="e3217-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e3217-2500">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="e3217-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e3217-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e3217-2501">Az.EventGrid</span></span>
* <span data-ttu-id="e3217-2502">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e3217-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e3217-2503">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e3217-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e3217-2504">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e3217-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e3217-2505">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="e3217-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e3217-2506">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="e3217-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e3217-2507">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="e3217-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e3217-2508">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e3217-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e3217-2509">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="e3217-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e3217-2510">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="e3217-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e3217-2511">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="e3217-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="e3217-2512">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e3217-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e3217-2513">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3217-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e3217-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2514">Az.IotHub</span></span>
* <span data-ttu-id="e3217-2515">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="e3217-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e3217-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e3217-2516">Az.LogicApp</span></span>
* <span data-ttu-id="e3217-2517">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="e3217-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2518">Az.Resources</span></span>
* <span data-ttu-id="e3217-2519">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="e3217-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e3217-2520">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e3217-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e3217-2521">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3217-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e3217-2522">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e3217-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e3217-2523">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="e3217-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e3217-2524">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e3217-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e3217-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e3217-2525">Az.SignalR</span></span>
* <span data-ttu-id="e3217-2526">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2527">Az.Sql</span></span>
* <span data-ttu-id="e3217-2528">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="e3217-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e3217-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2529">Az.Storage</span></span>
* <span data-ttu-id="e3217-2530">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="e3217-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e3217-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3217-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="e3217-2532">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="e3217-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e3217-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e3217-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2534">Az.Websites</span></span>
* <span data-ttu-id="e3217-2535">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="e3217-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e3217-2536">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e3217-2537">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e3217-2538">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-2538">General</span></span>

- <span data-ttu-id="e3217-2539">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="e3217-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="e3217-2540">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="e3217-2540">Online help for each module</span></span>
- <span data-ttu-id="e3217-2541">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e3217-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e3217-2542">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="e3217-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e3217-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2543">Az.Accounts</span></span>
- <span data-ttu-id="e3217-2544">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e3217-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="e3217-2545">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="e3217-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e3217-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="e3217-2547">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="e3217-2547">Fixes for #7002</span></span>
- <span data-ttu-id="e3217-2548">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e3217-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e3217-2549">Az.Batch</span></span>
- <span data-ttu-id="e3217-2550">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e3217-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e3217-2551">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="e3217-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e3217-2552">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e3217-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e3217-2553">Az.Billing</span></span>
- <span data-ttu-id="e3217-2554">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e3217-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="e3217-2556">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e3217-2557">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e3217-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e3217-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="e3217-2559">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e3217-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e3217-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e3217-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e3217-2561">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="e3217-2563">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e3217-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e3217-2564">Az.Monitor</span></span>
- <span data-ttu-id="e3217-2565">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e3217-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e3217-2566">Az.KeyVault</span></span>
- <span data-ttu-id="e3217-2567">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="e3217-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e3217-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e3217-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="e3217-2569">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e3217-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e3217-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e3217-2570">Az.Media</span></span>
- <span data-ttu-id="e3217-2571">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e3217-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e3217-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2572">Az.Network</span></span>
<span data-ttu-id="e3217-2573">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3217-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e3217-2574">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e3217-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="e3217-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e3217-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e3217-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3217-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e3217-2583">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3217-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e3217-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3217-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e3217-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e3217-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e3217-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e3217-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e3217-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e3217-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="e3217-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e3217-2590">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e3217-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e3217-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3217-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e3217-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3217-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e3217-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3217-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e3217-2594">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e3217-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e3217-2595">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e3217-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="e3217-2597">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e3217-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e3217-2598">Az.Profile</span></span>
- <span data-ttu-id="e3217-2599">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e3217-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="e3217-2601">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e3217-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2602">Az.Resources</span></span>
- <span data-ttu-id="e3217-2603">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e3217-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="e3217-2605">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="e3217-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e3217-2606">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e3217-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e3217-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="e3217-2608">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e3217-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e3217-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2609">Az.Sql</span></span>
- <span data-ttu-id="e3217-2610">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="e3217-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e3217-2611">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="e3217-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e3217-2612">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e3217-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2613">Az.Storage</span></span>
- <span data-ttu-id="e3217-2614">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e3217-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2615">Az.Websites</span></span>
- <span data-ttu-id="e3217-2616">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e3217-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e3217-2617">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e3217-2618">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-2618">General</span></span>

* <span data-ttu-id="e3217-2619">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e3217-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e3217-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2620">Az.Compute</span></span>

* <span data-ttu-id="e3217-2621">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="e3217-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="e3217-2623">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="e3217-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e3217-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e3217-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="e3217-2625">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="e3217-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="e3217-2626">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e3217-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e3217-2627">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e3217-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e3217-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="e3217-2629">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e3217-2630">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="e3217-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e3217-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2631">Az.Resources</span></span>

* <span data-ttu-id="e3217-2632">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e3217-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e3217-2633">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="e3217-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e3217-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2634">Az.Sql</span></span>

* <span data-ttu-id="e3217-2635">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e3217-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e3217-2636">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="e3217-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e3217-2637">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="e3217-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e3217-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2638">Az.Storage</span></span>

* <span data-ttu-id="e3217-2639">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e3217-2640">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="e3217-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e3217-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e3217-2642">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="e3217-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="e3217-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e3217-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e3217-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e3217-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e3217-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2645">Az.Websites</span></span>

* <span data-ttu-id="e3217-2646">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e3217-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="e3217-2647">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="e3217-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e3217-2648">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3217-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e3217-2649">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e3217-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e3217-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="e3217-2651">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e3217-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e3217-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e3217-2652">Az.Automation</span></span>
* <span data-ttu-id="e3217-2653">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="e3217-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e3217-2654">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e3217-2655">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e3217-2656">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="e3217-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e3217-2657">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="e3217-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e3217-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2658">Az.Compute</span></span>
* <span data-ttu-id="e3217-2659">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e3217-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e3217-2660">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e3217-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e3217-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="e3217-2662">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e3217-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e3217-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e3217-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e3217-2664">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="e3217-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e3217-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2665">Az.Network</span></span>
* <span data-ttu-id="e3217-2666">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e3217-2667">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="e3217-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e3217-2668">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="e3217-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="e3217-2669">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3217-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e3217-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e3217-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e3217-2671">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="e3217-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e3217-2672">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="e3217-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e3217-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e3217-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e3217-2674">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e3217-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e3217-2675">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e3217-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e3217-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e3217-2676">Az.Relay</span></span>
* <span data-ttu-id="e3217-2677">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e3217-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e3217-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2678">Az.Resources</span></span>
* <span data-ttu-id="e3217-2679">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e3217-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e3217-2680">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="e3217-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e3217-2681">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e3217-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e3217-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-2683">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="e3217-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e3217-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2684">Az.Sql</span></span>
* <span data-ttu-id="e3217-2685">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="e3217-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e3217-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e3217-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e3217-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e3217-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e3217-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e3217-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e3217-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e3217-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e3217-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e3217-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e3217-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e3217-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e3217-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e3217-2694">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e3217-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e3217-2695">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="e3217-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e3217-2696">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="e3217-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e3217-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e3217-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e3217-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e3217-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e3217-2699">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e3217-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e3217-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e3217-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e3217-2701">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e3217-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e3217-2702">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e3217-2703">Geral</span><span class="sxs-lookup"><span data-stu-id="e3217-2703">General</span></span>
* <span data-ttu-id="e3217-2704">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="e3217-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e3217-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e3217-2705">Az.Profile</span></span>
* <span data-ttu-id="e3217-2706">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e3217-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e3217-2707">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="e3217-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e3217-2708">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e3217-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e3217-2709">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="e3217-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e3217-2710">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="e3217-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e3217-2711">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="e3217-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e3217-2712">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="e3217-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-2714">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e3217-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2715">Az.Compute</span></span>
* <span data-ttu-id="e3217-2716">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e3217-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e3217-2717">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e3217-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e3217-2718">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="e3217-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2720">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e3217-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e3217-2721">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="e3217-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e3217-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e3217-2722">Az.Insights</span></span>
* <span data-ttu-id="e3217-2723">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="e3217-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e3217-2724">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="e3217-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e3217-2725">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="e3217-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e3217-2726">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="e3217-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2727">Az.Network</span></span>
* <span data-ttu-id="e3217-2728">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="e3217-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e3217-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e3217-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e3217-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e3217-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e3217-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e3217-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e3217-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e3217-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e3217-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e3217-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e3217-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e3217-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e3217-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="e3217-2736">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="e3217-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2737">Az.Resources</span></span>
* <span data-ttu-id="e3217-2738">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e3217-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e3217-2739">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="e3217-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e3217-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e3217-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="e3217-2741">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="e3217-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e3217-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e3217-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="e3217-2743">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="e3217-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e3217-2744">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="e3217-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e3217-2745">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e3217-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e3217-2746">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e3217-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e3217-2747">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="e3217-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e3217-2748">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e3217-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e3217-2749">Az.Profile</span></span>
* <span data-ttu-id="e3217-2750">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="e3217-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e3217-2751">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e3217-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2752">Az.Compute</span></span>
* <span data-ttu-id="e3217-2753">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="e3217-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e3217-2754">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e3217-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e3217-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e3217-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="e3217-2756">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e3217-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e3217-2757">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3217-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e3217-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="e3217-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e3217-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="e3217-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e3217-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3217-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2761">Az.Network</span></span>
* <span data-ttu-id="e3217-2762">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="e3217-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e3217-2763">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e3217-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2764">Az.Resources</span></span>
* <span data-ttu-id="e3217-2765">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="e3217-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e3217-2766">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="e3217-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e3217-2767">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e3217-2768">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e3217-2768">Azure.Storage</span></span>
* <span data-ttu-id="e3217-2769">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="e3217-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e3217-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e3217-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e3217-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e3217-2772">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e3217-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e3217-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e3217-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e3217-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e3217-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="e3217-2775">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="e3217-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e3217-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e3217-2776">Az.Compute</span></span>
* <span data-ttu-id="e3217-2777">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="e3217-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e3217-2778">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e3217-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e3217-2779">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="e3217-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e3217-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e3217-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e3217-2781">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e3217-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e3217-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e3217-2782">Az.Network</span></span>
* <span data-ttu-id="e3217-2783">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e3217-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e3217-2784">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="e3217-2784">new cmdlets added</span></span>
    - <span data-ttu-id="e3217-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e3217-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e3217-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e3217-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e3217-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e3217-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e3217-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e3217-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e3217-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e3217-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e3217-2791">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="e3217-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e3217-2792">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3217-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e3217-2793">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e3217-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e3217-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e3217-2794">Az.RedisCache</span></span>
* <span data-ttu-id="e3217-2795">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="e3217-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e3217-2796">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e3217-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e3217-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e3217-2797">Az.Resources</span></span>
* <span data-ttu-id="e3217-2798">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3217-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e3217-2799">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="e3217-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e3217-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e3217-2800">Az.Sql</span></span>
* <span data-ttu-id="e3217-2801">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="e3217-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e3217-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e3217-2802">Az.Websites</span></span>
* <span data-ttu-id="e3217-2803">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="e3217-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e3217-2804">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="e3217-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e3217-2805">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e3217-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e3217-2806">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="e3217-2806">Initial Release</span></span>
