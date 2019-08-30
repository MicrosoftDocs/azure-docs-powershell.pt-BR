---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052627"
---
## <a name="260---august-2019"></a><span data-ttu-id="7c3a2-101">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7c3a2-102">Geral</span><span class="sxs-lookup"><span data-stu-id="7c3a2-102">General</span></span>
* <span data-ttu-id="7c3a2-103">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-104">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-105">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7c3a2-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7c3a2-106">Az.Aks</span></span>
* <span data-ttu-id="7c3a2-107">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7c3a2-108">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7c3a2-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7c3a2-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-109">Az.ApiManagement</span></span>
* <span data-ttu-id="7c3a2-110">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="7c3a2-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7c3a2-111">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="7c3a2-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7c3a2-112">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7c3a2-113">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7c3a2-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7c3a2-114">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7c3a2-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7c3a2-115">Az.Batch</span></span>
* <span data-ttu-id="7c3a2-116">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="7c3a2-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7c3a2-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7c3a2-117">Az.Cdn</span></span>
* <span data-ttu-id="7c3a2-118">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="7c3a2-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-119">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-120">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7c3a2-121">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7c3a2-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7c3a2-122">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7c3a2-123">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7c3a2-124">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7c3a2-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7c3a2-125">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7c3a2-126">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="7c3a2-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7c3a2-127">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-128">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-129">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7c3a2-130">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="7c3a2-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7c3a2-131">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="7c3a2-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7c3a2-132">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="7c3a2-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-134">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7c3a2-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-135">Az.EventHub</span></span>
* <span data-ttu-id="7c3a2-136">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7c3a2-137">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="7c3a2-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7c3a2-138">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7c3a2-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7c3a2-139">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="7c3a2-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7c3a2-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7c3a2-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7c3a2-141">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7c3a2-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-142">Az.Monitor</span></span>
* <span data-ttu-id="7c3a2-143">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="7c3a2-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-144">Az.Network</span></span>
* <span data-ttu-id="7c3a2-145">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7c3a2-146">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7c3a2-147">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7c3a2-148">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="7c3a2-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7c3a2-149">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7c3a2-150">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7c3a2-151">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="7c3a2-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-153">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7c3a2-154">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-154">Added example</span></span>
    - <span data-ttu-id="7c3a2-155">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7c3a2-156">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7c3a2-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7c3a2-157">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7c3a2-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-159">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-160">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-161">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="7c3a2-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7c3a2-162">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="7c3a2-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7c3a2-163">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7c3a2-164">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="7c3a2-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-165">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-166">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7c3a2-167">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="7c3a2-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7c3a2-168">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="7c3a2-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-170">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7c3a2-171">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7c3a2-172">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7c3a2-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7c3a2-173">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7c3a2-174">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7c3a2-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7c3a2-175">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="7c3a2-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-176">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-177">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-178">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-179">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c3a2-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7c3a2-180">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="7c3a2-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7c3a2-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7c3a2-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7c3a2-183">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="7c3a2-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7c3a2-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-185">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-186">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c3a2-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7c3a2-187">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-188">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-189">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7c3a2-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7c3a2-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7c3a2-191">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-192">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-193">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-195">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-196">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-197">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7c3a2-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c3a2-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7c3a2-199">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7c3a2-200">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="7c3a2-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-201">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-202">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7c3a2-203">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="7c3a2-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7c3a2-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-204">Az.EventHub</span></span>
* <span data-ttu-id="7c3a2-205">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7c3a2-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7c3a2-206">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="7c3a2-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-207">Az.KeyVault</span></span>
* <span data-ttu-id="7c3a2-208">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7c3a2-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-209">Az.LogicApp</span></span>
* <span data-ttu-id="7c3a2-210">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="7c3a2-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7c3a2-211">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="7c3a2-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7c3a2-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-212">Az.ManagedServices</span></span>
* <span data-ttu-id="7c3a2-213">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-214">Az.Network</span></span>
* <span data-ttu-id="7c3a2-215">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7c3a2-216">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-216">New cmdlets</span></span>
        - <span data-ttu-id="7c3a2-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c3a2-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7c3a2-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7c3a2-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7c3a2-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7c3a2-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7c3a2-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7c3a2-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7c3a2-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7c3a2-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7c3a2-225">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="7c3a2-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7c3a2-226">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7c3a2-227">Parâmetro opcional -PrivateEndpointNetworkPoliciesFlag adicionado para indicar que habilitar ou desabilitar aplica políticas de rede no ponto de extremidade privado nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="7c3a2-228">Parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag adicionado para indicar que habilitar ou desabilitar aplica políticas de rede no serviço de link privado nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7c3a2-229">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="7c3a2-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7c3a2-230">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="7c3a2-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7c3a2-231">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-231">Updated cmdlets</span></span>
        - <span data-ttu-id="7c3a2-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7c3a2-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7c3a2-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7c3a2-235">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7c3a2-236">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7c3a2-237">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="7c3a2-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7c3a2-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7c3a2-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7c3a2-241">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7c3a2-242">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7c3a2-243">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-245">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7c3a2-246">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="7c3a2-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-248">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7c3a2-249">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7c3a2-250">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7c3a2-251">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7c3a2-252">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7c3a2-253">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7c3a2-254">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7c3a2-255">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7c3a2-256">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7c3a2-257">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-258">Az.Resources</span></span>
- <span data-ttu-id="7c3a2-259">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7c3a2-260">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7c3a2-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-261">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-262">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7c3a2-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7c3a2-263">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="7c3a2-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-264">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-265">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7c3a2-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7c3a2-266">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="7c3a2-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7c3a2-267">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-268">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-269">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="7c3a2-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7c3a2-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7c3a2-270">Az.StorageSync</span></span>
* <span data-ttu-id="7c3a2-271">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7c3a2-272">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="7c3a2-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-273">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-274">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7c3a2-275">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7c3a2-276">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7c3a2-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7c3a2-277">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-278">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-279">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="7c3a2-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7c3a2-280">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7c3a2-281">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c3a2-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7c3a2-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-282">Az.Advisor</span></span>
* <span data-ttu-id="7c3a2-283">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7c3a2-284">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7c3a2-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-285">Az.ApiManagement</span></span>
* <span data-ttu-id="7c3a2-286">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="7c3a2-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7c3a2-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7c3a2-288">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="7c3a2-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7c3a2-289">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7c3a2-290">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="7c3a2-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7c3a2-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7c3a2-292">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="7c3a2-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-293">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-294">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-295">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-296">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-297">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-298">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7c3a2-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c3a2-299">Az.EventGrid</span></span>
* <span data-ttu-id="7c3a2-300">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7c3a2-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-301">Az.IotHub</span></span>
* <span data-ttu-id="7c3a2-302">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-303">Az.Network</span></span>
* <span data-ttu-id="7c3a2-304">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="7c3a2-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7c3a2-305">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7c3a2-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="7c3a2-307">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7c3a2-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7c3a2-308">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7c3a2-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-310">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7c3a2-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-312">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="7c3a2-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-313">Az.Resources</span></span>
    - <span data-ttu-id="7c3a2-314">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="7c3a2-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7c3a2-315">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="7c3a2-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7c3a2-316">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="7c3a2-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7c3a2-317">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-318">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-319">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-320">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-321">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="7c3a2-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7c3a2-322">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7c3a2-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7c3a2-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7c3a2-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7c3a2-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7c3a2-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7c3a2-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7c3a2-329">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="7c3a2-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-330">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-331">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7c3a2-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7c3a2-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7c3a2-333">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7c3a2-334">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="7c3a2-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7c3a2-335">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7c3a2-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7c3a2-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7c3a2-338">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7c3a2-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7c3a2-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7c3a2-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7c3a2-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7c3a2-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7c3a2-341">Az.StorageSync</span></span>
* <span data-ttu-id="7c3a2-342">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7c3a2-343">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-344">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-345">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="7c3a2-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7c3a2-346">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7c3a2-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7c3a2-347">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="7c3a2-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7c3a2-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7c3a2-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7c3a2-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7c3a2-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-350">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-351">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7c3a2-352">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7c3a2-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7c3a2-353">Az.Dns</span></span>
* <span data-ttu-id="7c3a2-354">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7c3a2-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c3a2-355">Az.EventGrid</span></span>
* <span data-ttu-id="7c3a2-356">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7c3a2-357">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-357">New cmdlets:</span></span>
    - <span data-ttu-id="7c3a2-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7c3a2-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7c3a2-359">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7c3a2-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7c3a2-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7c3a2-361">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7c3a2-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7c3a2-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7c3a2-363">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7c3a2-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7c3a2-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7c3a2-365">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7c3a2-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7c3a2-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7c3a2-367">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7c3a2-368">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7c3a2-369">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7c3a2-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7c3a2-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7c3a2-371">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="7c3a2-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7c3a2-372">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7c3a2-373">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7c3a2-374">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="7c3a2-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7c3a2-376">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7c3a2-377">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7c3a2-378">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="7c3a2-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7c3a2-379">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7c3a2-380">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="7c3a2-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7c3a2-381">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7c3a2-382">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7c3a2-383">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="7c3a2-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7c3a2-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7c3a2-385">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7c3a2-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7c3a2-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7c3a2-387">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7c3a2-388">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7c3a2-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-389">Az.FrontDoor</span></span>
* <span data-ttu-id="7c3a2-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7c3a2-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7c3a2-391">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7c3a2-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7c3a2-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7c3a2-393">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="7c3a2-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-394">Az.Network</span></span>
* <span data-ttu-id="7c3a2-395">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7c3a2-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7c3a2-396">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-396">New cmdlets</span></span>
        - <span data-ttu-id="7c3a2-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7c3a2-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7c3a2-398">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7c3a2-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7c3a2-399">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-399">New cmdlets</span></span> 
        - <span data-ttu-id="7c3a2-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7c3a2-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7c3a2-401">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7c3a2-402">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-402">New cmdlets</span></span> 
        - <span data-ttu-id="7c3a2-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7c3a2-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7c3a2-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7c3a2-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7c3a2-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7c3a2-408">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c3a2-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7c3a2-409">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-409">New cmdlets</span></span>
        - <span data-ttu-id="7c3a2-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c3a2-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7c3a2-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c3a2-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7c3a2-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7c3a2-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7c3a2-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7c3a2-414">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7c3a2-415">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7c3a2-416">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7c3a2-417">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7c3a2-418">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7c3a2-419">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7c3a2-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7c3a2-420">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7c3a2-421">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7c3a2-422">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7c3a2-423">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7c3a2-424">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7c3a2-425">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7c3a2-426">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="7c3a2-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7c3a2-427">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7c3a2-428">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7c3a2-429">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="7c3a2-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7c3a2-430">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="7c3a2-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7c3a2-431">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7c3a2-432">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7c3a2-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7c3a2-433">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7c3a2-434">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7c3a2-435">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7c3a2-436">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-438">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-439">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-440">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7c3a2-441">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7c3a2-442">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7c3a2-443">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-445">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-446">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-447">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7c3a2-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7c3a2-448">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7c3a2-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7c3a2-449">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7c3a2-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7c3a2-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7c3a2-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7c3a2-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7c3a2-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7c3a2-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7c3a2-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7c3a2-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7c3a2-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7c3a2-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-455">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-456">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7c3a2-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7c3a2-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="7c3a2-458">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="7c3a2-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7c3a2-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-460">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-461">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="7c3a2-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7c3a2-462">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7c3a2-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7c3a2-463">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7c3a2-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7c3a2-464">Az.Cdn</span></span>
* <span data-ttu-id="7c3a2-465">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-466">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-467">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7c3a2-468">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7c3a2-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-469">Az.EventHub</span></span>
* <span data-ttu-id="7c3a2-470">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7c3a2-471">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3a2-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-472">Az.Network</span></span>
* <span data-ttu-id="7c3a2-473">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="7c3a2-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7c3a2-474">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="7c3a2-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7c3a2-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="7c3a2-476">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-478">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="7c3a2-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-479">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-480">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3a2-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-482">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7c3a2-483">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-484">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-485">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7c3a2-486">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7c3a2-487">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7c3a2-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7c3a2-488">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-489">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-490">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7c3a2-491">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7c3a2-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-492">Az.ApiManagement</span></span>
* <span data-ttu-id="7c3a2-493">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7c3a2-494">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7c3a2-495">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7c3a2-496">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7c3a2-497">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7c3a2-498">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7c3a2-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7c3a2-499">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7c3a2-500">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7c3a2-501">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7c3a2-502">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="7c3a2-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7c3a2-503">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7c3a2-504">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="7c3a2-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7c3a2-505">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="7c3a2-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7c3a2-506">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7c3a2-507">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7c3a2-508">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7c3a2-509">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7c3a2-510">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="7c3a2-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7c3a2-511">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7c3a2-512">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="7c3a2-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7c3a2-513">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="7c3a2-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7c3a2-514">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7c3a2-515">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7c3a2-516">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7c3a2-517">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7c3a2-518">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7c3a2-519">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7c3a2-520">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7c3a2-521">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7c3a2-522">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7c3a2-523">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7c3a2-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7c3a2-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7c3a2-525">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7c3a2-526">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7c3a2-527">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7c3a2-528">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="7c3a2-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7c3a2-529">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7c3a2-530">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7c3a2-531">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7c3a2-532">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7c3a2-533">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7c3a2-534">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7c3a2-535">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7c3a2-536">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7c3a2-537">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7c3a2-538">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7c3a2-539">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7c3a2-540">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7c3a2-541">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7c3a2-542">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7c3a2-543">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7c3a2-544">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7c3a2-545">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7c3a2-546">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7c3a2-547">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7c3a2-548">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7c3a2-549">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7c3a2-550">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7c3a2-551">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7c3a2-552">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7c3a2-553">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7c3a2-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7c3a2-554">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7c3a2-555">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7c3a2-556">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7c3a2-557">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7c3a2-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7c3a2-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7c3a2-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7c3a2-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7c3a2-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7c3a2-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7c3a2-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7c3a2-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7c3a2-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7c3a2-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7c3a2-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7c3a2-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7c3a2-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7c3a2-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7c3a2-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-570">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-571">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7c3a2-572">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="7c3a2-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7c3a2-573">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="7c3a2-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7c3a2-574">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7c3a2-575">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="7c3a2-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7c3a2-576">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7c3a2-577">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-578">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-579">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7c3a2-580">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-582">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7c3a2-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-583">Az.Monitor</span></span>
* <span data-ttu-id="7c3a2-584">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="7c3a2-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-585">Az.Network</span></span>
* <span data-ttu-id="7c3a2-586">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7c3a2-587">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="7c3a2-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7c3a2-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7c3a2-589">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7c3a2-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-590">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-591">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-592">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-593">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="7c3a2-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7c3a2-594">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-595">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-596">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="7c3a2-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-598">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7c3a2-599">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-600">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-601">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7c3a2-602">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7c3a2-603">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7c3a2-604">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7c3a2-605">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7c3a2-606">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7c3a2-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7c3a2-607">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="7c3a2-607">Breaking changes</span></span>
    - <span data-ttu-id="7c3a2-608">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7c3a2-609">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7c3a2-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7c3a2-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="7c3a2-611">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7c3a2-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7c3a2-612">Az.Dns</span></span>
* <span data-ttu-id="7c3a2-613">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="7c3a2-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7c3a2-614">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7c3a2-615">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7c3a2-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-616">Az.FrontDoor</span></span>
* <span data-ttu-id="7c3a2-617">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7c3a2-618">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7c3a2-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c3a2-619">Az.HDInsight</span></span>
* <span data-ttu-id="7c3a2-620">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7c3a2-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7c3a2-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7c3a2-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7c3a2-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7c3a2-623">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7c3a2-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7c3a2-624">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7c3a2-625">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7c3a2-626">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7c3a2-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-627">Az.Monitor</span></span>
* <span data-ttu-id="7c3a2-628">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7c3a2-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7c3a2-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7c3a2-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7c3a2-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7c3a2-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7c3a2-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7c3a2-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7c3a2-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7c3a2-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7c3a2-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7c3a2-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7c3a2-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7c3a2-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7c3a2-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7c3a2-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7c3a2-640">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="7c3a2-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7c3a2-641">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-642">Az.Network</span></span>
* <span data-ttu-id="7c3a2-643">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="7c3a2-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7c3a2-644">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7c3a2-644">New cmdlets</span></span>
        - <span data-ttu-id="7c3a2-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="7c3a2-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7c3a2-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7c3a2-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7c3a2-649">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-649">Updated cmdlets</span></span>
        - <span data-ttu-id="7c3a2-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7c3a2-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7c3a2-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7c3a2-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7c3a2-652">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7c3a2-653">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7c3a2-654">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7c3a2-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="7c3a2-656">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7c3a2-657">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7c3a2-658">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-660">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7c3a2-661">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7c3a2-662">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7c3a2-663">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7c3a2-664">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7c3a2-665">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7c3a2-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7c3a2-666">Az.Relay</span></span>
* <span data-ttu-id="7c3a2-667">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="7c3a2-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-668">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-669">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="7c3a2-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-670">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-671">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="7c3a2-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7c3a2-672">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7c3a2-673">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7c3a2-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="7c3a2-675">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7c3a2-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7c3a2-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7c3a2-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-679">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-680">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7c3a2-681">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7c3a2-682">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7c3a2-683">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7c3a2-683">Highlights since the last major release</span></span>
* <span data-ttu-id="7c3a2-684">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-684">General availability of `Az` module</span></span>
* <span data-ttu-id="7c3a2-685">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7c3a2-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7c3a2-686">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7c3a2-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7c3a2-687">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7c3a2-688">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7c3a2-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7c3a2-689">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7c3a2-690">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7c3a2-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-691">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-692">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="7c3a2-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7c3a2-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7c3a2-693">Az.Batch</span></span>
* <span data-ttu-id="7c3a2-694">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7c3a2-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7c3a2-695">Az.Cdn</span></span>
* <span data-ttu-id="7c3a2-696">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-698">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-699">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-700">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7c3a2-701">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-702">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7c3a2-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-703">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-704">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-706">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7c3a2-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c3a2-707">Az.EventGrid</span></span>
* <span data-ttu-id="7c3a2-708">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7c3a2-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-709">Az.EventHub</span></span>
* <span data-ttu-id="7c3a2-710">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="7c3a2-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7c3a2-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7c3a2-711">Az.HDInsight</span></span>
* <span data-ttu-id="7c3a2-712">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7c3a2-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-713">Az.IotHub</span></span>
* <span data-ttu-id="7c3a2-714">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-715">Az.KeyVault</span></span>
* <span data-ttu-id="7c3a2-716">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-717">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7c3a2-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7c3a2-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7c3a2-718">Az.MachineLearning</span></span>
* <span data-ttu-id="7c3a2-719">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7c3a2-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7c3a2-720">Az.Media</span></span>
* <span data-ttu-id="7c3a2-721">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7c3a2-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-722">Az.Monitor</span></span>
  * <span data-ttu-id="7c3a2-723">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7c3a2-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7c3a2-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7c3a2-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7c3a2-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7c3a2-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7c3a2-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7c3a2-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7c3a2-729">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="7c3a2-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-730">Az.Network</span></span>
* <span data-ttu-id="7c3a2-731">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-732">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7c3a2-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7c3a2-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7c3a2-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="7c3a2-734">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-736">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7c3a2-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7c3a2-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7c3a2-738">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-740">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-741">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7c3a2-742">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="7c3a2-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7c3a2-743">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="7c3a2-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7c3a2-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7c3a2-744">Az.RedisCache</span></span>
* <span data-ttu-id="7c3a2-745">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-746">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-747">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7c3a2-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-748">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-749">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="7c3a2-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7c3a2-750">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-751">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7c3a2-752">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7c3a2-753">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7c3a2-754">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7c3a2-755">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7c3a2-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-756">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-757">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="7c3a2-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7c3a2-758">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7c3a2-759">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7c3a2-760">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7c3a2-761">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7c3a2-762">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7c3a2-762">Highlights since the last major release</span></span>
* <span data-ttu-id="7c3a2-763">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-763">General availability of `Az` module</span></span>
* <span data-ttu-id="7c3a2-764">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7c3a2-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7c3a2-765">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7c3a2-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7c3a2-766">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7c3a2-767">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7c3a2-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7c3a2-768">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7c3a2-769">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7c3a2-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-770">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-771">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7c3a2-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7c3a2-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="7c3a2-773">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="7c3a2-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7c3a2-774">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="7c3a2-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-775">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-776">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7c3a2-777">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7c3a2-778">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-779">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-780">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7c3a2-781">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7c3a2-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="7c3a2-783">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="7c3a2-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-784">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-785">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7c3a2-786">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-787">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-788">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="7c3a2-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7c3a2-789">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7c3a2-790">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="7c3a2-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7c3a2-791">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7c3a2-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7c3a2-792">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="7c3a2-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7c3a2-793">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7c3a2-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-794">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-795">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-796">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-797">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7c3a2-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c3a2-798">New-AzStorageContext</span></span>
* <span data-ttu-id="7c3a2-799">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7c3a2-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7c3a2-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7c3a2-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7c3a2-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7c3a2-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7c3a2-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7c3a2-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7c3a2-804">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7c3a2-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7c3a2-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7c3a2-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7c3a2-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7c3a2-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7c3a2-809">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7c3a2-810">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7c3a2-810">Highlights since the last major release</span></span>
* <span data-ttu-id="7c3a2-811">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-811">General availability of `Az` module</span></span>
* <span data-ttu-id="7c3a2-812">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7c3a2-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7c3a2-813">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7c3a2-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7c3a2-814">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7c3a2-815">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7c3a2-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7c3a2-816">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7c3a2-817">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7c3a2-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-818">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-819">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7c3a2-820">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="7c3a2-820">Dynamic grouping</span></span>
    * <span data-ttu-id="7c3a2-821">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-821">Pre-Post script</span></span>
    * <span data-ttu-id="7c3a2-822">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="7c3a2-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-823">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-824">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7c3a2-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7c3a2-825">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-826">Az.KeyVault</span></span>
* <span data-ttu-id="7c3a2-827">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-828">Az.Network</span></span>
* <span data-ttu-id="7c3a2-829">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7c3a2-830">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-832">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7c3a2-833">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="7c3a2-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-834">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-835">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7c3a2-836">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-837">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-838">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-839">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-840">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="7c3a2-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7c3a2-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7c3a2-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7c3a2-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7c3a2-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7c3a2-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7c3a2-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7c3a2-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7c3a2-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-847">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-848">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="7c3a2-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7c3a2-849">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-850">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-851">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="7c3a2-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7c3a2-852">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-853">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-854">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7c3a2-855">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7c3a2-856">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="7c3a2-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7c3a2-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7c3a2-857">Az.Cdn</span></span>
* <span data-ttu-id="7c3a2-858">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-859">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-860">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="7c3a2-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-861">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-862">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="7c3a2-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7c3a2-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-863">Az.LogicApp</span></span>
* <span data-ttu-id="7c3a2-864">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-865">Az.Network</span></span>
* <span data-ttu-id="7c3a2-866">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-868">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7c3a2-869">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="7c3a2-869">SDK Update</span></span>
* <span data-ttu-id="7c3a2-870">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7c3a2-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7c3a2-871">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7c3a2-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-872">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-873">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7c3a2-874">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7c3a2-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7c3a2-875">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7c3a2-876">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7c3a2-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7c3a2-877">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7c3a2-878">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7c3a2-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-879">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-880">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7c3a2-881">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-882">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-883">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7c3a2-884">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7c3a2-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="7c3a2-886">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-887">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-888">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7c3a2-889">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7c3a2-890">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-892">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-893">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-894">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="7c3a2-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7c3a2-895">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="7c3a2-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7c3a2-896">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7c3a2-897">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-899">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7c3a2-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-900">Az.EventHub</span></span>
* <span data-ttu-id="7c3a2-901">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-902">Az.KeyVault</span></span>
* <span data-ttu-id="7c3a2-903">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7c3a2-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7c3a2-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-904">Az.LogicApp</span></span>
* <span data-ttu-id="7c3a2-905">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="7c3a2-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7c3a2-906">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="7c3a2-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7c3a2-907">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="7c3a2-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7c3a2-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7c3a2-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7c3a2-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7c3a2-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7c3a2-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7c3a2-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7c3a2-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7c3a2-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7c3a2-912">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="7c3a2-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7c3a2-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7c3a2-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7c3a2-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7c3a2-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7c3a2-917">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7c3a2-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7c3a2-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-918">Az.Monitor</span></span>
* <span data-ttu-id="7c3a2-919">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-920">Az.Network</span></span>
* <span data-ttu-id="7c3a2-921">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7c3a2-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="7c3a2-923">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7c3a2-924">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7c3a2-925">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7c3a2-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-926">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-927">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7c3a2-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7c3a2-928">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7c3a2-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7c3a2-929">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7c3a2-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7c3a2-930">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="7c3a2-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-931">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-932">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7c3a2-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7c3a2-933">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="7c3a2-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-934">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-935">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="7c3a2-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7c3a2-936">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-937">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-938">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7c3a2-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7c3a2-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-939">Az.AnalysisServices</span></span>
<span data-ttu-id="7c3a2-940">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-941">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-942">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="7c3a2-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7c3a2-943">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7c3a2-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7c3a2-944">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-945">Az.RecoveryServices</span></span>
<span data-ttu-id="7c3a2-946">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-947">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-948">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7c3a2-949">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7c3a2-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7c3a2-950">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="7c3a2-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7c3a2-951">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7c3a2-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-952">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-953">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7c3a2-954">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="7c3a2-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7c3a2-955">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="7c3a2-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7c3a2-956">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-957">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-958">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="7c3a2-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7c3a2-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="7c3a2-960">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="7c3a2-962">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7c3a2-963">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-964">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-965">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7c3a2-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7c3a2-966">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7c3a2-967">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="7c3a2-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7c3a2-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7c3a2-968">Az.Aks</span></span>
* <span data-ttu-id="7c3a2-969">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7c3a2-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-970">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-971">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7c3a2-972">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7c3a2-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7c3a2-973">Az.Cdn</span></span>
* <span data-ttu-id="7c3a2-974">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-975">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-976">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7c3a2-977">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7c3a2-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7c3a2-978">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7c3a2-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7c3a2-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7c3a2-980">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7c3a2-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c3a2-981">Az.DataFactory</span></span>
* <span data-ttu-id="7c3a2-982">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="7c3a2-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-984">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="7c3a2-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7c3a2-985">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7c3a2-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7c3a2-986">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7c3a2-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-987">Az.IotHub</span></span>
* <span data-ttu-id="7c3a2-988">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-989">Az.KeyVault</span></span>
* <span data-ttu-id="7c3a2-990">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-991">Az.Network</span></span>
* <span data-ttu-id="7c3a2-992">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-993">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-994">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7c3a2-995">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7c3a2-996">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="7c3a2-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7c3a2-997">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7c3a2-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7c3a2-998">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7c3a2-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7c3a2-999">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7c3a2-1000">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-1002">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7c3a2-1003">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1003">Fix some error messages.</span></span>
* <span data-ttu-id="7c3a2-1004">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7c3a2-1005">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7c3a2-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1006">Az.SignalR</span></span>
* <span data-ttu-id="7c3a2-1007">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1008">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-1009">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7c3a2-1010">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7c3a2-1011">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7c3a2-1012">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1013">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-1014">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7c3a2-1015">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7c3a2-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7c3a2-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7c3a2-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="7c3a2-1019">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1020">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-1021">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7c3a2-1022">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7c3a2-1023">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7c3a2-1024">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7c3a2-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1025">Az.Accounts</span></span>
* <span data-ttu-id="7c3a2-1026">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1027">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-1028">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7c3a2-1029">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7c3a2-1030">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-1032">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7c3a2-1033">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7c3a2-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1034">Az.EventGrid</span></span>
* <span data-ttu-id="7c3a2-1035">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7c3a2-1036">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7c3a2-1037">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7c3a2-1038">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7c3a2-1039">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7c3a2-1040">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7c3a2-1041">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7c3a2-1042">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7c3a2-1043">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7c3a2-1044">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="7c3a2-1045">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7c3a2-1046">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7c3a2-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1047">Az.IotHub</span></span>
* <span data-ttu-id="7c3a2-1048">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7c3a2-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1049">Az.LogicApp</span></span>
* <span data-ttu-id="7c3a2-1050">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1051">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-1052">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7c3a2-1053">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7c3a2-1054">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7c3a2-1055">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7c3a2-1056">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7c3a2-1057">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7c3a2-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1058">Az.SignalR</span></span>
* <span data-ttu-id="7c3a2-1059">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1060">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-1061">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7c3a2-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1062">Az.Storage</span></span>
* <span data-ttu-id="7c3a2-1063">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7c3a2-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="7c3a2-1065">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7c3a2-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1067">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-1068">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7c3a2-1069">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7c3a2-1070">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7c3a2-1071">Geral</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1071">General</span></span>

- <span data-ttu-id="7c3a2-1072">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="7c3a2-1073">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1073">Online help for each module</span></span>
- <span data-ttu-id="7c3a2-1074">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7c3a2-1075">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7c3a2-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1076">Az.Accounts</span></span>
- <span data-ttu-id="7c3a2-1077">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="7c3a2-1078">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7c3a2-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="7c3a2-1080">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1080">Fixes for #7002</span></span>
- <span data-ttu-id="7c3a2-1081">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7c3a2-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1082">Az.Batch</span></span>
- <span data-ttu-id="7c3a2-1083">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7c3a2-1084">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7c3a2-1085">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7c3a2-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1086">Az.Billing</span></span>
- <span data-ttu-id="7c3a2-1087">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7c3a2-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="7c3a2-1089">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7c3a2-1090">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7c3a2-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="7c3a2-1092">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7c3a2-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7c3a2-1094">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="7c3a2-1096">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7c3a2-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1097">Az.Monitor</span></span>
- <span data-ttu-id="7c3a2-1098">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7c3a2-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1099">Az.KeyVault</span></span>
- <span data-ttu-id="7c3a2-1100">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7c3a2-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="7c3a2-1102">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7c3a2-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1103">Az.Media</span></span>
- <span data-ttu-id="7c3a2-1104">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7c3a2-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1105">Az.Network</span></span>
<span data-ttu-id="7c3a2-1106">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7c3a2-1107">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="7c3a2-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7c3a2-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7c3a2-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7c3a2-1116">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7c3a2-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7c3a2-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7c3a2-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7c3a2-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7c3a2-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7c3a2-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7c3a2-1123">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7c3a2-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7c3a2-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7c3a2-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7c3a2-1127">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7c3a2-1128">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7c3a2-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="7c3a2-1130">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7c3a2-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1131">Az.Profile</span></span>
- <span data-ttu-id="7c3a2-1132">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="7c3a2-1134">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7c3a2-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1135">Az.Resources</span></span>
- <span data-ttu-id="7c3a2-1136">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="7c3a2-1138">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7c3a2-1139">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7c3a2-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="7c3a2-1141">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7c3a2-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1142">Az.Sql</span></span>
- <span data-ttu-id="7c3a2-1143">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7c3a2-1144">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7c3a2-1145">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7c3a2-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1146">Az.Storage</span></span>
- <span data-ttu-id="7c3a2-1147">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7c3a2-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1148">Az.Websites</span></span>
- <span data-ttu-id="7c3a2-1149">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7c3a2-1150">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7c3a2-1151">Geral</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1151">General</span></span>

* <span data-ttu-id="7c3a2-1152">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7c3a2-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1153">Az.Compute</span></span>

* <span data-ttu-id="7c3a2-1154">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="7c3a2-1156">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7c3a2-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="7c3a2-1158">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="7c3a2-1159">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7c3a2-1160">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7c3a2-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="7c3a2-1162">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7c3a2-1163">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7c3a2-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1164">Az.Resources</span></span>

* <span data-ttu-id="7c3a2-1165">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7c3a2-1166">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7c3a2-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1167">Az.Sql</span></span>

* <span data-ttu-id="7c3a2-1168">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7c3a2-1169">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7c3a2-1170">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7c3a2-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1171">Az.Storage</span></span>

* <span data-ttu-id="7c3a2-1172">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7c3a2-1173">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7c3a2-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7c3a2-1175">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="7c3a2-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7c3a2-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7c3a2-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1178">Az.Websites</span></span>

* <span data-ttu-id="7c3a2-1179">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7c3a2-1180">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7c3a2-1181">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7c3a2-1182">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7c3a2-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="7c3a2-1184">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7c3a2-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1185">Az.Automation</span></span>
* <span data-ttu-id="7c3a2-1186">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7c3a2-1187">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7c3a2-1188">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7c3a2-1189">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7c3a2-1190">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7c3a2-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1191">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-1192">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7c3a2-1193">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7c3a2-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="7c3a2-1195">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7c3a2-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7c3a2-1197">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7c3a2-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1198">Az.Network</span></span>
* <span data-ttu-id="7c3a2-1199">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7c3a2-1200">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7c3a2-1201">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7c3a2-1202">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7c3a2-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7c3a2-1204">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7c3a2-1205">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7c3a2-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7c3a2-1207">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7c3a2-1208">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7c3a2-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1209">Az.Relay</span></span>
* <span data-ttu-id="7c3a2-1210">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7c3a2-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1211">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-1212">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7c3a2-1213">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7c3a2-1214">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-1216">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7c3a2-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1217">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-1218">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7c3a2-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7c3a2-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7c3a2-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7c3a2-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7c3a2-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7c3a2-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7c3a2-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7c3a2-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7c3a2-1227">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7c3a2-1228">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7c3a2-1229">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7c3a2-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7c3a2-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7c3a2-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7c3a2-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7c3a2-1234">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7c3a2-1235">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7c3a2-1236">Geral</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1236">General</span></span>
* <span data-ttu-id="7c3a2-1237">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7c3a2-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1238">Az.Profile</span></span>
* <span data-ttu-id="7c3a2-1239">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7c3a2-1240">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7c3a2-1241">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7c3a2-1242">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7c3a2-1243">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7c3a2-1244">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7c3a2-1245">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-1247">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1248">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-1249">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7c3a2-1250">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7c3a2-1251">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-1253">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7c3a2-1254">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7c3a2-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1255">Az.Insights</span></span>
* <span data-ttu-id="7c3a2-1256">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7c3a2-1257">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7c3a2-1258">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7c3a2-1259">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1260">Az.Network</span></span>
* <span data-ttu-id="7c3a2-1261">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7c3a2-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7c3a2-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7c3a2-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7c3a2-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7c3a2-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7c3a2-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7c3a2-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="7c3a2-1269">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1270">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-1271">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7c3a2-1272">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7c3a2-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="7c3a2-1274">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7c3a2-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="7c3a2-1276">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7c3a2-1277">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7c3a2-1278">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7c3a2-1279">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7c3a2-1280">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7c3a2-1281">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7c3a2-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1282">Az.Profile</span></span>
* <span data-ttu-id="7c3a2-1283">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7c3a2-1284">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1285">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-1286">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7c3a2-1287">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7c3a2-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="7c3a2-1289">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7c3a2-1290">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7c3a2-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7c3a2-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7c3a2-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1294">Az.Network</span></span>
* <span data-ttu-id="7c3a2-1295">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7c3a2-1296">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1297">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-1298">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7c3a2-1299">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7c3a2-1300">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7c3a2-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1301">Azure.Storage</span></span>
* <span data-ttu-id="7c3a2-1302">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7c3a2-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7c3a2-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7c3a2-1305">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7c3a2-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7c3a2-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="7c3a2-1308">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7c3a2-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1309">Az.Compute</span></span>
* <span data-ttu-id="7c3a2-1310">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7c3a2-1311">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7c3a2-1312">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7c3a2-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7c3a2-1314">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7c3a2-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1315">Az.Network</span></span>
* <span data-ttu-id="7c3a2-1316">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7c3a2-1317">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1317">new cmdlets added</span></span>
    - <span data-ttu-id="7c3a2-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7c3a2-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7c3a2-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7c3a2-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7c3a2-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7c3a2-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7c3a2-1324">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7c3a2-1325">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7c3a2-1326">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7c3a2-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1327">Az.RedisCache</span></span>
* <span data-ttu-id="7c3a2-1328">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7c3a2-1329">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7c3a2-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1330">Az.Resources</span></span>
* <span data-ttu-id="7c3a2-1331">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7c3a2-1332">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7c3a2-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1333">Az.Sql</span></span>
* <span data-ttu-id="7c3a2-1334">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7c3a2-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1335">Az.Websites</span></span>
* <span data-ttu-id="7c3a2-1336">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7c3a2-1337">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7c3a2-1338">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7c3a2-1339">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="7c3a2-1339">Initial Release</span></span>