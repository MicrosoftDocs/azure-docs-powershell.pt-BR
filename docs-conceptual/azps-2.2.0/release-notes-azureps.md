---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498668"
---
## <a name="220---june-2019"></a><span data-ttu-id="d8f11-101">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d8f11-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d8f11-102">Az.Cdn</span></span>
* <span data-ttu-id="d8f11-103">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d8f11-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-104">Az.Compute</span></span>
* <span data-ttu-id="d8f11-105">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d8f11-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d8f11-106">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d8f11-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d8f11-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-107">Az.EventHub</span></span>
* <span data-ttu-id="d8f11-108">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="d8f11-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d8f11-109">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f11-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-110">Az.Network</span></span>
* <span data-ttu-id="d8f11-111">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="d8f11-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d8f11-112">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f11-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d8f11-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="d8f11-114">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d8f11-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-116">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="d8f11-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d8f11-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d8f11-117">Az.ServiceBus</span></span>
* <span data-ttu-id="d8f11-118">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f11-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d8f11-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="d8f11-120">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d8f11-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d8f11-121">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-122">Az.Sql</span></span>
* <span data-ttu-id="d8f11-123">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d8f11-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d8f11-124">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d8f11-125">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d8f11-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d8f11-126">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="d8f11-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-127">Az.Websites</span></span>
* <span data-ttu-id="d8f11-128">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="d8f11-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d8f11-129">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d8f11-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d8f11-130">Az.ApiManagement</span></span>
* <span data-ttu-id="d8f11-131">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d8f11-132">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d8f11-133">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d8f11-134">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="d8f11-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d8f11-135">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8f11-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d8f11-136">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d8f11-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d8f11-137">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d8f11-138">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d8f11-139">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d8f11-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d8f11-140">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="d8f11-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d8f11-141">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d8f11-142">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="d8f11-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d8f11-143">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="d8f11-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d8f11-144">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="d8f11-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d8f11-145">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="d8f11-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d8f11-146">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="d8f11-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d8f11-147">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d8f11-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d8f11-148">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d8f11-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d8f11-149">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="d8f11-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d8f11-150">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="d8f11-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d8f11-151">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="d8f11-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d8f11-152">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="d8f11-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d8f11-153">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="d8f11-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d8f11-154">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d8f11-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d8f11-155">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d8f11-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d8f11-156">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d8f11-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d8f11-157">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d8f11-158">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d8f11-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d8f11-159">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d8f11-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d8f11-160">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="d8f11-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d8f11-161">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="d8f11-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d8f11-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d8f11-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d8f11-163">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d8f11-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d8f11-164">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d8f11-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d8f11-165">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d8f11-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d8f11-166">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="d8f11-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d8f11-167">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="d8f11-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d8f11-168">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="d8f11-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d8f11-169">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="d8f11-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d8f11-170">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d8f11-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d8f11-171">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d8f11-172">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d8f11-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d8f11-173">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d8f11-174">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d8f11-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d8f11-175">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d8f11-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d8f11-176">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d8f11-177">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d8f11-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d8f11-178">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d8f11-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d8f11-179">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="d8f11-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d8f11-180">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d8f11-181">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="d8f11-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d8f11-182">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="d8f11-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d8f11-183">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="d8f11-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d8f11-184">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="d8f11-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d8f11-185">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="d8f11-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d8f11-186">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="d8f11-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d8f11-187">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d8f11-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d8f11-188">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d8f11-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d8f11-189">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d8f11-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d8f11-190">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8f11-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d8f11-191">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d8f11-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d8f11-192">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d8f11-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d8f11-193">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d8f11-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d8f11-194">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8f11-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d8f11-195">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="d8f11-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d8f11-196">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d8f11-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d8f11-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d8f11-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d8f11-198">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d8f11-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d8f11-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d8f11-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d8f11-200">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d8f11-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d8f11-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d8f11-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d8f11-202">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d8f11-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d8f11-203">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d8f11-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d8f11-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d8f11-205">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d8f11-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d8f11-206">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d8f11-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d8f11-207">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d8f11-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-208">Az.Automation</span></span>
* <span data-ttu-id="d8f11-209">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="d8f11-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d8f11-210">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d8f11-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d8f11-211">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d8f11-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d8f11-212">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="d8f11-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d8f11-213">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d8f11-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d8f11-214">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="d8f11-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d8f11-215">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="d8f11-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-216">Az.Compute</span></span>
* <span data-ttu-id="d8f11-217">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d8f11-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d8f11-218">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="d8f11-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-220">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d8f11-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d8f11-221">Az.Monitor</span></span>
* <span data-ttu-id="d8f11-222">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="d8f11-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-223">Az.Network</span></span>
* <span data-ttu-id="d8f11-224">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="d8f11-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d8f11-225">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d8f11-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="d8f11-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d8f11-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d8f11-227">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d8f11-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-228">Az.Resources</span></span>
* <span data-ttu-id="d8f11-229">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="d8f11-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-230">Az.Sql</span></span>
* <span data-ttu-id="d8f11-231">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="d8f11-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d8f11-232">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-233">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-234">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="d8f11-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d8f11-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="d8f11-236">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="d8f11-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d8f11-237">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="d8f11-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-238">Az.Compute</span></span>
* <span data-ttu-id="d8f11-239">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="d8f11-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d8f11-240">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d8f11-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d8f11-241">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d8f11-242">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d8f11-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d8f11-243">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d8f11-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d8f11-244">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d8f11-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d8f11-245">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="d8f11-245">Breaking changes</span></span>
    - <span data-ttu-id="d8f11-246">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d8f11-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d8f11-247">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d8f11-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d8f11-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d8f11-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="d8f11-249">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d8f11-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d8f11-250">Az.Dns</span></span>
* <span data-ttu-id="d8f11-251">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="d8f11-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d8f11-252">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="d8f11-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d8f11-253">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d8f11-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d8f11-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d8f11-254">Az.FrontDoor</span></span>
* <span data-ttu-id="d8f11-255">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d8f11-256">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="d8f11-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d8f11-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d8f11-257">Az.HDInsight</span></span>
* <span data-ttu-id="d8f11-258">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d8f11-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d8f11-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d8f11-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d8f11-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d8f11-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d8f11-261">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d8f11-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d8f11-262">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="d8f11-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d8f11-263">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="d8f11-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d8f11-264">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="d8f11-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d8f11-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d8f11-265">Az.Monitor</span></span>
* <span data-ttu-id="d8f11-266">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d8f11-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d8f11-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d8f11-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d8f11-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d8f11-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d8f11-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d8f11-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d8f11-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d8f11-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d8f11-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d8f11-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d8f11-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d8f11-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d8f11-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d8f11-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d8f11-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d8f11-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d8f11-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d8f11-278">[Mais](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="d8f11-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d8f11-279">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d8f11-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-280">Az.Network</span></span>
* <span data-ttu-id="d8f11-281">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="d8f11-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d8f11-282">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d8f11-282">New cmdlets</span></span>
        - <span data-ttu-id="d8f11-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d8f11-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="d8f11-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d8f11-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d8f11-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d8f11-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d8f11-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d8f11-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d8f11-287">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d8f11-287">Updated cmdlets</span></span>
        - <span data-ttu-id="d8f11-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d8f11-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d8f11-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d8f11-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d8f11-290">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="d8f11-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d8f11-291">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8f11-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d8f11-292">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8f11-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d8f11-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="d8f11-294">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="d8f11-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d8f11-295">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d8f11-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d8f11-296">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-298">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d8f11-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d8f11-299">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d8f11-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d8f11-300">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d8f11-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d8f11-301">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f11-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d8f11-302">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d8f11-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d8f11-303">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="d8f11-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d8f11-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d8f11-304">Az.Relay</span></span>
* <span data-ttu-id="d8f11-305">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="d8f11-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d8f11-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d8f11-306">Az.ServiceBus</span></span>
* <span data-ttu-id="d8f11-307">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d8f11-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-308">Az.Storage</span></span>
* <span data-ttu-id="d8f11-309">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="d8f11-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d8f11-310">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="d8f11-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d8f11-311">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="d8f11-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d8f11-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="d8f11-313">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="d8f11-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d8f11-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d8f11-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d8f11-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-317">Az.Websites</span></span>
* <span data-ttu-id="d8f11-318">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d8f11-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d8f11-319">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="d8f11-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d8f11-320">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d8f11-321">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d8f11-321">Highlights since the last major release</span></span>
* <span data-ttu-id="d8f11-322">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d8f11-322">General availability of `Az` module</span></span>
* <span data-ttu-id="d8f11-323">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d8f11-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d8f11-324">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d8f11-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d8f11-325">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d8f11-326">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d8f11-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d8f11-327">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d8f11-328">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d8f11-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d8f11-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-329">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-330">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="d8f11-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d8f11-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d8f11-331">Az.Batch</span></span>
* <span data-ttu-id="d8f11-332">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d8f11-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d8f11-333">Az.Cdn</span></span>
* <span data-ttu-id="d8f11-334">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d8f11-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="d8f11-336">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-337">Az.Compute</span></span>
* <span data-ttu-id="d8f11-338">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="d8f11-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d8f11-339">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-340">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d8f11-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d8f11-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8f11-341">Az.DataFactory</span></span>
* <span data-ttu-id="d8f11-342">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d8f11-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-344">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d8f11-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d8f11-345">Az.EventGrid</span></span>
* <span data-ttu-id="d8f11-346">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="d8f11-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d8f11-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-347">Az.EventHub</span></span>
* <span data-ttu-id="d8f11-348">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d8f11-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d8f11-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d8f11-349">Az.HDInsight</span></span>
* <span data-ttu-id="d8f11-350">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d8f11-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-351">Az.IotHub</span></span>
* <span data-ttu-id="d8f11-352">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d8f11-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-353">Az.KeyVault</span></span>
* <span data-ttu-id="d8f11-354">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-355">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d8f11-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d8f11-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d8f11-356">Az.MachineLearning</span></span>
* <span data-ttu-id="d8f11-357">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d8f11-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d8f11-358">Az.Media</span></span>
* <span data-ttu-id="d8f11-359">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d8f11-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d8f11-360">Az.Monitor</span></span>
  * <span data-ttu-id="d8f11-361">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d8f11-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d8f11-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d8f11-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d8f11-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d8f11-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d8f11-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d8f11-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d8f11-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d8f11-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d8f11-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d8f11-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d8f11-367">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="d8f11-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-368">Az.Network</span></span>
* <span data-ttu-id="d8f11-369">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-370">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d8f11-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d8f11-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d8f11-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="d8f11-372">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d8f11-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="d8f11-374">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d8f11-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d8f11-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d8f11-376">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-378">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-379">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d8f11-380">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d8f11-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d8f11-381">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="d8f11-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d8f11-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d8f11-382">Az.RedisCache</span></span>
* <span data-ttu-id="d8f11-383">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-384">Az.Resources</span></span>
* <span data-ttu-id="d8f11-385">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d8f11-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-386">Az.Sql</span></span>
* <span data-ttu-id="d8f11-387">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="d8f11-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d8f11-388">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-389">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d8f11-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d8f11-390">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="d8f11-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d8f11-391">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="d8f11-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d8f11-392">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d8f11-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d8f11-393">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d8f11-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-394">Az.Websites</span></span>
* <span data-ttu-id="d8f11-395">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="d8f11-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d8f11-396">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d8f11-397">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="d8f11-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d8f11-398">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d8f11-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d8f11-399">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d8f11-400">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d8f11-400">Highlights since the last major release</span></span>
* <span data-ttu-id="d8f11-401">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d8f11-401">General availability of `Az` module</span></span>
* <span data-ttu-id="d8f11-402">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d8f11-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d8f11-403">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d8f11-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d8f11-404">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d8f11-405">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d8f11-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d8f11-406">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d8f11-407">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d8f11-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d8f11-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-408">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-409">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f11-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d8f11-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="d8f11-411">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="d8f11-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d8f11-412">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="d8f11-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-413">Az.Automation</span></span>
* <span data-ttu-id="d8f11-414">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="d8f11-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d8f11-415">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="d8f11-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d8f11-416">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-417">Az.Compute</span></span>
* <span data-ttu-id="d8f11-418">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d8f11-419">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="d8f11-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d8f11-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="d8f11-421">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="d8f11-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d8f11-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8f11-422">Az.DataFactory</span></span>
* <span data-ttu-id="d8f11-423">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="d8f11-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d8f11-424">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8f11-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-425">Az.Resources</span></span>
* <span data-ttu-id="d8f11-426">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="d8f11-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d8f11-427">Melhorar o tratamento de erros para “Test-AzDeployment” e “Test-AzResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="d8f11-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d8f11-428">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="d8f11-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d8f11-429">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d8f11-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d8f11-430">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="d8f11-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d8f11-431">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d8f11-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-432">Az.Sql</span></span>
* <span data-ttu-id="d8f11-433">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="d8f11-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-434">Az.Storage</span></span>
* <span data-ttu-id="d8f11-435">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d8f11-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8f11-436">New-AzStorageContext</span></span>
* <span data-ttu-id="d8f11-437">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d8f11-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d8f11-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d8f11-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d8f11-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d8f11-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d8f11-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d8f11-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d8f11-442">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="d8f11-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d8f11-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d8f11-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d8f11-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d8f11-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d8f11-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d8f11-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d8f11-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d8f11-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d8f11-447">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d8f11-448">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d8f11-448">Highlights since the last major release</span></span>
* <span data-ttu-id="d8f11-449">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d8f11-449">General availability of `Az` module</span></span>
* <span data-ttu-id="d8f11-450">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d8f11-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d8f11-451">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d8f11-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d8f11-452">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d8f11-453">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d8f11-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d8f11-454">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d8f11-455">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d8f11-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-456">Az.Automation</span></span>
* <span data-ttu-id="d8f11-457">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d8f11-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d8f11-458">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="d8f11-458">Dynamic grouping</span></span>
    * <span data-ttu-id="d8f11-459">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="d8f11-459">Pre-Post script</span></span>
    * <span data-ttu-id="d8f11-460">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="d8f11-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-461">Az.Compute</span></span>
* <span data-ttu-id="d8f11-462">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d8f11-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d8f11-463">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d8f11-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d8f11-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-464">Az.KeyVault</span></span>
* <span data-ttu-id="d8f11-465">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-466">Az.Network</span></span>
* <span data-ttu-id="d8f11-467">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d8f11-468">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="d8f11-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-470">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="d8f11-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d8f11-471">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d8f11-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-472">Az.Resources</span></span>
* <span data-ttu-id="d8f11-473">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8f11-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d8f11-474">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="d8f11-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-475">Az.Sql</span></span>
* <span data-ttu-id="d8f11-476">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="d8f11-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-477">Az.Storage</span></span>
* <span data-ttu-id="d8f11-478">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d8f11-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d8f11-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d8f11-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d8f11-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d8f11-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d8f11-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d8f11-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d8f11-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d8f11-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-485">Az.Websites</span></span>
* <span data-ttu-id="d8f11-486">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="d8f11-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d8f11-487">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-488">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-489">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="d8f11-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d8f11-490">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-491">Az.Automation</span></span>
* <span data-ttu-id="d8f11-492">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d8f11-493">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="d8f11-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d8f11-494">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="d8f11-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d8f11-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d8f11-495">Az.Cdn</span></span>
* <span data-ttu-id="d8f11-496">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="d8f11-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-497">Az.Compute</span></span>
* <span data-ttu-id="d8f11-498">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="d8f11-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d8f11-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8f11-499">Az.DataFactory</span></span>
* <span data-ttu-id="d8f11-500">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="d8f11-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d8f11-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d8f11-501">Az.LogicApp</span></span>
* <span data-ttu-id="d8f11-502">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="d8f11-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-503">Az.Network</span></span>
* <span data-ttu-id="d8f11-504">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-506">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d8f11-507">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="d8f11-507">SDK Update</span></span>
* <span data-ttu-id="d8f11-508">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d8f11-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d8f11-509">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d8f11-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-510">Az.Resources</span></span>
* <span data-ttu-id="d8f11-511">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="d8f11-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d8f11-512">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d8f11-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d8f11-513">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d8f11-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d8f11-514">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d8f11-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d8f11-515">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d8f11-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d8f11-516">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d8f11-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-517">Az.Sql</span></span>
* <span data-ttu-id="d8f11-518">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d8f11-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d8f11-519">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d8f11-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-520">Az.Storage</span></span>
* <span data-ttu-id="d8f11-521">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d8f11-522">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d8f11-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="d8f11-524">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-525">Az.Automation</span></span>
* <span data-ttu-id="d8f11-526">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d8f11-527">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d8f11-528">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d8f11-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="d8f11-530">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8f11-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-531">Az.Compute</span></span>
* <span data-ttu-id="d8f11-532">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="d8f11-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d8f11-533">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="d8f11-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d8f11-534">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d8f11-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d8f11-535">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="d8f11-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-537">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="d8f11-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d8f11-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-538">Az.EventHub</span></span>
* <span data-ttu-id="d8f11-539">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d8f11-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-540">Az.KeyVault</span></span>
* <span data-ttu-id="d8f11-541">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d8f11-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d8f11-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d8f11-542">Az.LogicApp</span></span>
* <span data-ttu-id="d8f11-543">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="d8f11-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d8f11-544">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="d8f11-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d8f11-545">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d8f11-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d8f11-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8f11-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d8f11-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8f11-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d8f11-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8f11-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d8f11-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d8f11-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d8f11-550">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="d8f11-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d8f11-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d8f11-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d8f11-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d8f11-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d8f11-555">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d8f11-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d8f11-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d8f11-556">Az.Monitor</span></span>
* <span data-ttu-id="d8f11-557">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="d8f11-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-558">Az.Network</span></span>
* <span data-ttu-id="d8f11-559">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d8f11-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d8f11-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="d8f11-561">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="d8f11-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d8f11-562">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="d8f11-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d8f11-563">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="d8f11-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d8f11-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-564">Az.Resources</span></span>
* <span data-ttu-id="d8f11-565">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d8f11-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d8f11-566">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d8f11-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d8f11-567">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d8f11-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d8f11-568">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d8f11-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-569">Az.Sql</span></span>
* <span data-ttu-id="d8f11-570">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d8f11-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d8f11-571">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="d8f11-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-572">Az.Websites</span></span>
* <span data-ttu-id="d8f11-573">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d8f11-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d8f11-574">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-575">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-576">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d8f11-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d8f11-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-577">Az.AnalysisServices</span></span>
<span data-ttu-id="d8f11-578">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d8f11-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-579">Az.Compute</span></span>
* <span data-ttu-id="d8f11-580">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="d8f11-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d8f11-581">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d8f11-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d8f11-582">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d8f11-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-583">Az.RecoveryServices</span></span>
<span data-ttu-id="d8f11-584">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d8f11-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-585">Az.Resources</span></span>
* <span data-ttu-id="d8f11-586">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="d8f11-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d8f11-587">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d8f11-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d8f11-588">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="d8f11-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d8f11-589">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d8f11-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-590">Az.Sql</span></span>
* <span data-ttu-id="d8f11-591">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d8f11-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d8f11-592">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="d8f11-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d8f11-593">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d8f11-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d8f11-594">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-595">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-596">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="d8f11-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d8f11-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="d8f11-598">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d8f11-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="d8f11-600">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d8f11-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d8f11-601">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-602">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-603">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d8f11-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d8f11-604">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d8f11-605">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d8f11-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d8f11-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d8f11-606">Az.Aks</span></span>
* <span data-ttu-id="d8f11-607">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d8f11-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-608">Az.Automation</span></span>
* <span data-ttu-id="d8f11-609">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="d8f11-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d8f11-610">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d8f11-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d8f11-611">Az.Cdn</span></span>
* <span data-ttu-id="d8f11-612">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-613">Az.Compute</span></span>
* <span data-ttu-id="d8f11-614">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="d8f11-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d8f11-615">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d8f11-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d8f11-616">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d8f11-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d8f11-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8f11-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d8f11-618">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d8f11-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d8f11-619">Az.DataFactory</span></span>
* <span data-ttu-id="d8f11-620">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d8f11-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-622">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d8f11-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d8f11-623">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d8f11-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d8f11-624">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d8f11-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-625">Az.IotHub</span></span>
* <span data-ttu-id="d8f11-626">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d8f11-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d8f11-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-627">Az.KeyVault</span></span>
* <span data-ttu-id="d8f11-628">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-629">Az.Network</span></span>
* <span data-ttu-id="d8f11-630">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-631">Az.Resources</span></span>
* <span data-ttu-id="d8f11-632">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="d8f11-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d8f11-633">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d8f11-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d8f11-634">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="d8f11-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d8f11-635">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d8f11-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d8f11-636">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d8f11-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d8f11-637">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d8f11-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d8f11-638">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d8f11-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d8f11-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="d8f11-640">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d8f11-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d8f11-641">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="d8f11-641">Fix some error messages.</span></span>
* <span data-ttu-id="d8f11-642">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="d8f11-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d8f11-643">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="d8f11-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d8f11-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d8f11-644">Az.SignalR</span></span>
* <span data-ttu-id="d8f11-645">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-646">Az.Sql</span></span>
* <span data-ttu-id="d8f11-647">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d8f11-648">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d8f11-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d8f11-649">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="d8f11-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d8f11-650">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d8f11-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-651">Az.Storage</span></span>
* <span data-ttu-id="d8f11-652">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d8f11-653">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d8f11-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d8f11-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d8f11-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d8f11-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d8f11-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d8f11-656">Az.TrafficManager</span></span>
* <span data-ttu-id="d8f11-657">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-658">Az.Websites</span></span>
* <span data-ttu-id="d8f11-659">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d8f11-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d8f11-660">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="d8f11-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d8f11-661">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="d8f11-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d8f11-662">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d8f11-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d8f11-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-663">Az.Accounts</span></span>
* <span data-ttu-id="d8f11-664">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="d8f11-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-665">Az.Compute</span></span>
* <span data-ttu-id="d8f11-666">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d8f11-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d8f11-667">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d8f11-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d8f11-668">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-670">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="d8f11-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d8f11-671">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="d8f11-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d8f11-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d8f11-672">Az.EventGrid</span></span>
* <span data-ttu-id="d8f11-673">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d8f11-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d8f11-674">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d8f11-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d8f11-675">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d8f11-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d8f11-676">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d8f11-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d8f11-677">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d8f11-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d8f11-678">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d8f11-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d8f11-679">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d8f11-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d8f11-680">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d8f11-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d8f11-681">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d8f11-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d8f11-682">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d8f11-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="d8f11-683">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d8f11-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d8f11-684">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8f11-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d8f11-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-685">Az.IotHub</span></span>
* <span data-ttu-id="d8f11-686">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="d8f11-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d8f11-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d8f11-687">Az.LogicApp</span></span>
* <span data-ttu-id="d8f11-688">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="d8f11-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-689">Az.Resources</span></span>
* <span data-ttu-id="d8f11-690">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="d8f11-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d8f11-691">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d8f11-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d8f11-692">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8f11-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d8f11-693">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d8f11-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d8f11-694">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="d8f11-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d8f11-695">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d8f11-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d8f11-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d8f11-696">Az.SignalR</span></span>
* <span data-ttu-id="d8f11-697">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-698">Az.Sql</span></span>
* <span data-ttu-id="d8f11-699">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="d8f11-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d8f11-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-700">Az.Storage</span></span>
* <span data-ttu-id="d8f11-701">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="d8f11-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d8f11-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8f11-702">New-AzStorageContext</span></span>
* <span data-ttu-id="d8f11-703">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="d8f11-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d8f11-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d8f11-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-705">Az.Websites</span></span>
* <span data-ttu-id="d8f11-706">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="d8f11-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d8f11-707">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d8f11-708">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d8f11-709">Geral</span><span class="sxs-lookup"><span data-stu-id="d8f11-709">General</span></span>

- <span data-ttu-id="d8f11-710">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="d8f11-710">General Availability of Az Module</span></span>
- <span data-ttu-id="d8f11-711">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="d8f11-711">Online help for each module</span></span>
- <span data-ttu-id="d8f11-712">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="d8f11-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d8f11-713">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d8f11-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d8f11-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-714">Az.Accounts</span></span>
- <span data-ttu-id="d8f11-715">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d8f11-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="d8f11-716">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="d8f11-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d8f11-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d8f11-717">Az.ApiManagement</span></span>
- <span data-ttu-id="d8f11-718">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="d8f11-718">Fixes for #7002</span></span>
- <span data-ttu-id="d8f11-719">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d8f11-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d8f11-720">Az.Batch</span></span>
- <span data-ttu-id="d8f11-721">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d8f11-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d8f11-722">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="d8f11-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d8f11-723">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d8f11-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d8f11-724">Az.Billing</span></span>
- <span data-ttu-id="d8f11-725">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d8f11-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-726">Az.CognitivServices</span></span>
- <span data-ttu-id="d8f11-727">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d8f11-728">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="d8f11-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d8f11-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="d8f11-730">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d8f11-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d8f11-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d8f11-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d8f11-732">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="d8f11-734">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d8f11-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d8f11-735">Az.Monitor</span></span>
- <span data-ttu-id="d8f11-736">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d8f11-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d8f11-737">Az.KeyVault</span></span>
- <span data-ttu-id="d8f11-738">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="d8f11-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d8f11-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d8f11-739">Az.MachineLearning</span></span>
- <span data-ttu-id="d8f11-740">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d8f11-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d8f11-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d8f11-741">Az.Media</span></span>
- <span data-ttu-id="d8f11-742">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d8f11-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d8f11-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-743">Az.Network</span></span>
<span data-ttu-id="d8f11-744">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d8f11-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d8f11-745">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d8f11-745">New cmdlets added:</span></span>
        - <span data-ttu-id="d8f11-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d8f11-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d8f11-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8f11-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d8f11-754">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8f11-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d8f11-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8f11-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d8f11-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d8f11-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d8f11-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d8f11-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d8f11-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d8f11-760">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="d8f11-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d8f11-761">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d8f11-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d8f11-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8f11-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d8f11-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8f11-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d8f11-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8f11-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d8f11-765">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d8f11-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d8f11-766">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d8f11-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="d8f11-768">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d8f11-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d8f11-769">Az.Profile</span></span>
- <span data-ttu-id="d8f11-770">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d8f11-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="d8f11-772">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d8f11-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-773">Az.Resources</span></span>
- <span data-ttu-id="d8f11-774">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d8f11-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="d8f11-776">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="d8f11-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d8f11-777">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d8f11-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d8f11-778">Az.SIgnalR</span></span>
- <span data-ttu-id="d8f11-779">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d8f11-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d8f11-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-780">Az.Sql</span></span>
- <span data-ttu-id="d8f11-781">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="d8f11-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d8f11-782">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="d8f11-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d8f11-783">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d8f11-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-784">Az.Storage</span></span>
- <span data-ttu-id="d8f11-785">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d8f11-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-786">Az.Websites</span></span>
- <span data-ttu-id="d8f11-787">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d8f11-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d8f11-788">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d8f11-789">Geral</span><span class="sxs-lookup"><span data-stu-id="d8f11-789">General</span></span>

* <span data-ttu-id="d8f11-790">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d8f11-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d8f11-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-791">Az.Compute</span></span>

* <span data-ttu-id="d8f11-792">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d8f11-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="d8f11-794">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="d8f11-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d8f11-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d8f11-795">Az.FrontDoor</span></span>

* <span data-ttu-id="d8f11-796">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="d8f11-796">Fixed some broken links</span></span>
    - <span data-ttu-id="d8f11-797">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d8f11-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d8f11-798">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d8f11-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d8f11-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="d8f11-800">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d8f11-801">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="d8f11-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d8f11-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-802">Az.Resources</span></span>

* <span data-ttu-id="d8f11-803">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d8f11-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d8f11-804">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="d8f11-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d8f11-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-805">Az.Sql</span></span>

* <span data-ttu-id="d8f11-806">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d8f11-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d8f11-807">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="d8f11-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d8f11-808">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="d8f11-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d8f11-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-809">Az.Storage</span></span>

* <span data-ttu-id="d8f11-810">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d8f11-811">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="d8f11-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d8f11-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d8f11-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d8f11-813">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="d8f11-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="d8f11-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d8f11-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d8f11-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d8f11-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d8f11-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-816">Az.Websites</span></span>

* <span data-ttu-id="d8f11-817">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d8f11-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d8f11-818">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="d8f11-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d8f11-819">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f11-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d8f11-820">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d8f11-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d8f11-821">Az.ApiManagement</span></span>
* <span data-ttu-id="d8f11-822">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d8f11-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d8f11-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d8f11-823">Az.Automation</span></span>
* <span data-ttu-id="d8f11-824">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="d8f11-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d8f11-825">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="d8f11-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d8f11-826">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="d8f11-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d8f11-827">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="d8f11-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d8f11-828">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="d8f11-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d8f11-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-829">Az.Compute</span></span>
* <span data-ttu-id="d8f11-830">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d8f11-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d8f11-831">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d8f11-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d8f11-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="d8f11-833">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d8f11-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d8f11-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d8f11-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d8f11-835">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="d8f11-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d8f11-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-836">Az.Network</span></span>
* <span data-ttu-id="d8f11-837">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="d8f11-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d8f11-838">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f11-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d8f11-839">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="d8f11-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d8f11-840">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d8f11-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d8f11-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d8f11-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d8f11-842">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="d8f11-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d8f11-843">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="d8f11-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d8f11-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d8f11-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d8f11-845">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d8f11-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d8f11-846">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d8f11-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d8f11-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d8f11-847">Az.Relay</span></span>
* <span data-ttu-id="d8f11-848">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d8f11-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d8f11-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-849">Az.Resources</span></span>
* <span data-ttu-id="d8f11-850">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="d8f11-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d8f11-851">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="d8f11-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d8f11-852">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d8f11-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d8f11-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="d8f11-854">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="d8f11-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d8f11-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-855">Az.Sql</span></span>
* <span data-ttu-id="d8f11-856">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="d8f11-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d8f11-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d8f11-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d8f11-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d8f11-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d8f11-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d8f11-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d8f11-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d8f11-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d8f11-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d8f11-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d8f11-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d8f11-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d8f11-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d8f11-865">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8f11-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d8f11-866">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d8f11-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d8f11-867">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="d8f11-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d8f11-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d8f11-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d8f11-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d8f11-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d8f11-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d8f11-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d8f11-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d8f11-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d8f11-872">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d8f11-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d8f11-873">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d8f11-874">Geral</span><span class="sxs-lookup"><span data-stu-id="d8f11-874">General</span></span>
* <span data-ttu-id="d8f11-875">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="d8f11-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d8f11-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d8f11-876">Az.Profile</span></span>
* <span data-ttu-id="d8f11-877">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d8f11-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d8f11-878">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="d8f11-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d8f11-879">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d8f11-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d8f11-880">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="d8f11-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d8f11-881">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="d8f11-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d8f11-882">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d8f11-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d8f11-883">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="d8f11-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d8f11-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="d8f11-885">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d8f11-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-886">Az.Compute</span></span>
* <span data-ttu-id="d8f11-887">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d8f11-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d8f11-888">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d8f11-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d8f11-889">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="d8f11-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-891">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d8f11-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d8f11-892">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="d8f11-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d8f11-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d8f11-893">Az.Insights</span></span>
* <span data-ttu-id="d8f11-894">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="d8f11-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d8f11-895">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="d8f11-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d8f11-896">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="d8f11-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d8f11-897">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="d8f11-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-898">Az.Network</span></span>
* <span data-ttu-id="d8f11-899">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="d8f11-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d8f11-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d8f11-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d8f11-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d8f11-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d8f11-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d8f11-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d8f11-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d8f11-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d8f11-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d8f11-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d8f11-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d8f11-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d8f11-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d8f11-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="d8f11-907">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="d8f11-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-908">Az.Resources</span></span>
* <span data-ttu-id="d8f11-909">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d8f11-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d8f11-910">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="d8f11-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d8f11-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d8f11-911">Az.ServiceBus</span></span>
* <span data-ttu-id="d8f11-912">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="d8f11-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d8f11-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d8f11-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="d8f11-914">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="d8f11-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d8f11-915">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="d8f11-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d8f11-916">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d8f11-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d8f11-917">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d8f11-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d8f11-918">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="d8f11-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d8f11-919">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d8f11-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d8f11-920">Az.Profile</span></span>
* <span data-ttu-id="d8f11-921">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="d8f11-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d8f11-922">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d8f11-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-923">Az.Compute</span></span>
* <span data-ttu-id="d8f11-924">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="d8f11-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d8f11-925">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d8f11-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d8f11-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d8f11-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="d8f11-927">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d8f11-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d8f11-928">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8f11-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d8f11-929">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d8f11-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d8f11-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d8f11-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d8f11-931">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8f11-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-932">Az.Network</span></span>
* <span data-ttu-id="d8f11-933">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d8f11-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d8f11-934">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d8f11-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-935">Az.Resources</span></span>
* <span data-ttu-id="d8f11-936">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="d8f11-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d8f11-937">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="d8f11-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d8f11-938">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d8f11-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d8f11-939">Azure.Storage</span></span>
* <span data-ttu-id="d8f11-940">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="d8f11-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d8f11-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d8f11-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d8f11-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d8f11-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d8f11-943">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d8f11-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d8f11-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d8f11-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d8f11-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d8f11-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="d8f11-946">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="d8f11-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d8f11-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d8f11-947">Az.Compute</span></span>
* <span data-ttu-id="d8f11-948">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="d8f11-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d8f11-949">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d8f11-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d8f11-950">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="d8f11-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d8f11-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d8f11-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d8f11-952">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d8f11-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d8f11-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d8f11-953">Az.Network</span></span>
* <span data-ttu-id="d8f11-954">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d8f11-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d8f11-955">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="d8f11-955">new cmdlets added</span></span>
    - <span data-ttu-id="d8f11-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d8f11-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d8f11-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d8f11-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d8f11-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d8f11-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d8f11-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d8f11-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d8f11-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d8f11-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d8f11-962">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="d8f11-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d8f11-963">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d8f11-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d8f11-964">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d8f11-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d8f11-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d8f11-965">Az.RedisCache</span></span>
* <span data-ttu-id="d8f11-966">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="d8f11-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d8f11-967">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="d8f11-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d8f11-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d8f11-968">Az.Resources</span></span>
* <span data-ttu-id="d8f11-969">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d8f11-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d8f11-970">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="d8f11-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d8f11-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d8f11-971">Az.Sql</span></span>
* <span data-ttu-id="d8f11-972">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="d8f11-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d8f11-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d8f11-973">Az.Websites</span></span>
* <span data-ttu-id="d8f11-974">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="d8f11-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d8f11-975">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="d8f11-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d8f11-976">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d8f11-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d8f11-977">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="d8f11-977">Initial Release</span></span>