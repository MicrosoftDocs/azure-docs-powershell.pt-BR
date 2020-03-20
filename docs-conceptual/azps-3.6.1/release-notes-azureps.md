---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111036"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="37be6-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="37be6-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="37be6-104">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="37be6-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-105">Az.Accounts</span></span>
* <span data-ttu-id="37be6-106">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="37be6-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="37be6-107">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="37be6-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="37be6-108">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="37be6-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37be6-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-109">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-110">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="37be6-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="37be6-111">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="37be6-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="37be6-112">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="37be6-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="37be6-113">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="37be6-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-115">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="37be6-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-116">Az.IotHub</span></span>
* <span data-ttu-id="37be6-117">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="37be6-118">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="37be6-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="37be6-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="37be6-123">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="37be6-124">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="37be6-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="37be6-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="37be6-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="37be6-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="37be6-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="37be6-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="37be6-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="37be6-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="37be6-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="37be6-129">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="37be6-130">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="37be6-131">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="37be6-132">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="37be6-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="37be6-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="37be6-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="37be6-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="37be6-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="37be6-135">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37be6-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-136">Az.Monitor</span></span>
* <span data-ttu-id="37be6-137">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="37be6-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-138">Az.Network</span></span>
* <span data-ttu-id="37be6-139">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="37be6-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="37be6-140">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="37be6-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="37be6-141">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="37be6-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="37be6-142">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="37be6-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-143">Az.Resources</span></span>
* <span data-ttu-id="37be6-144">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="37be6-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="37be6-145">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="37be6-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="37be6-146">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="37be6-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="37be6-147">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="37be6-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="37be6-148">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="37be6-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="37be6-149">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="37be6-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="37be6-150">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="37be6-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="37be6-151">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="37be6-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="37be6-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="37be6-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="37be6-155">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="37be6-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="37be6-157">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="37be6-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-158">Az.Sql</span></span>
* <span data-ttu-id="37be6-159">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="37be6-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="37be6-160">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="37be6-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="37be6-161">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="37be6-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="37be6-162">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="37be6-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="37be6-163">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="37be6-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="37be6-164">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="37be6-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="37be6-165">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="37be6-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="37be6-166">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="37be6-167">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-168">Az.Storage</span></span>
* <span data-ttu-id="37be6-169">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="37be6-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="37be6-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="37be6-171">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="37be6-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="37be6-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="37be6-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="37be6-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="37be6-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-174">Az.Websites</span></span>
* <span data-ttu-id="37be6-175">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="37be6-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="37be6-176">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="37be6-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="37be6-177">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="37be6-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="37be6-178">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="37be6-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="37be6-179">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="37be6-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="37be6-180">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="37be6-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-181">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-181">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-182">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="37be6-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="37be6-183">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="37be6-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="37be6-184">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="37be6-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-185">Az.Accounts</span></span>
* <span data-ttu-id="37be6-186">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="37be6-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-187">Az.Automation</span></span>
* <span data-ttu-id="37be6-188">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="37be6-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-190">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="37be6-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="37be6-191">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="37be6-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-192">Az.Compute</span></span>
* <span data-ttu-id="37be6-193">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="37be6-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-194">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-195">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="37be6-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-196">Az.IotHub</span></span>
* <span data-ttu-id="37be6-197">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="37be6-198">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="37be6-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="37be6-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="37be6-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="37be6-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-203">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-204">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="37be6-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-205">Az.Monitor</span></span>
* <span data-ttu-id="37be6-206">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="37be6-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="37be6-207">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="37be6-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="37be6-208">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="37be6-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-209">Az.Network</span></span>
* <span data-ttu-id="37be6-210">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="37be6-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="37be6-211">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="37be6-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="37be6-212">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="37be6-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="37be6-213">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="37be6-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="37be6-214">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="37be6-214">No new cmdlets are added.</span></span> <span data-ttu-id="37be6-215">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="37be6-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-217">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="37be6-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-218">Az.Resources</span></span>
* <span data-ttu-id="37be6-219">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="37be6-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="37be6-220">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="37be6-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="37be6-221">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="37be6-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="37be6-222">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="37be6-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="37be6-223">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="37be6-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="37be6-224">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="37be6-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="37be6-225">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="37be6-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="37be6-226">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-227">Az.Sql</span></span>
* <span data-ttu-id="37be6-228">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="37be6-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="37be6-229">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="37be6-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="37be6-230">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="37be6-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="37be6-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="37be6-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="37be6-232">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="37be6-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37be6-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37be6-233">Az.StorageSync</span></span>
* <span data-ttu-id="37be6-234">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="37be6-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="37be6-235">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="37be6-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-236">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-236">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-237">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="37be6-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="37be6-238">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-239">Az.Accounts</span></span>
* <span data-ttu-id="37be6-240">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="37be6-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="37be6-241">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="37be6-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37be6-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-242">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-243">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="37be6-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="37be6-244">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="37be6-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="37be6-245">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="37be6-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="37be6-246">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="37be6-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-247">Az.Compute</span></span>
* <span data-ttu-id="37be6-248">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="37be6-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="37be6-249">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="37be6-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="37be6-250">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37be6-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="37be6-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="37be6-252">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="37be6-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-253">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-254">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="37be6-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="37be6-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="37be6-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="37be6-256">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="37be6-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="37be6-257">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="37be6-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37be6-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-258">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-259">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="37be6-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-260">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-261">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="37be6-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-262">Az.Network</span></span>
* <span data-ttu-id="37be6-263">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="37be6-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="37be6-264">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="37be6-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="37be6-265">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="37be6-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="37be6-266">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="37be6-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="37be6-267">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="37be6-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="37be6-268">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="37be6-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="37be6-269">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="37be6-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="37be6-270">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="37be6-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="37be6-271">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-271">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="37be6-273">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="37be6-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37be6-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="37be6-275">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="37be6-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37be6-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="37be6-277">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="37be6-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="37be6-278">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="37be6-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="37be6-279">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="37be6-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="37be6-280">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="37be6-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-282">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="37be6-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="37be6-283">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="37be6-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-284">Az.Resources</span></span>
* <span data-ttu-id="37be6-285">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="37be6-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="37be6-286">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="37be6-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-287">Az.Sql</span></span>
<span data-ttu-id="37be6-288">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="37be6-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-289">Az.Storage</span></span>
* <span data-ttu-id="37be6-290">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37be6-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="37be6-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="37be6-292">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="37be6-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="37be6-293">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-294">Az.Websites</span></span>
* <span data-ttu-id="37be6-295">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="37be6-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="37be6-296">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="37be6-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="37be6-297">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="37be6-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-298">Az.Accounts</span></span>
* <span data-ttu-id="37be6-299">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="37be6-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-300">Az.Cdn</span></span>
* <span data-ttu-id="37be6-301">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-302">Az.Compute</span></span>
* <span data-ttu-id="37be6-303">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="37be6-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="37be6-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="37be6-305">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="37be6-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="37be6-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="37be6-307">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="37be6-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37be6-308">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="37be6-309">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="37be6-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37be6-310">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="37be6-311">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="37be6-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37be6-312">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="37be6-313">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="37be6-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="37be6-314">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="37be6-315">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="37be6-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37be6-316">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="37be6-317">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="37be6-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37be6-318">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="37be6-319">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="37be6-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="37be6-320">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="37be6-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="37be6-321">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="37be6-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="37be6-322">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="37be6-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="37be6-323">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="37be6-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="37be6-324">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="37be6-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-325">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-326">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="37be6-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="37be6-327">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="37be6-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="37be6-328">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="37be6-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="37be6-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="37be6-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="37be6-330">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="37be6-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-331">Az.EventHub</span></span>
* <span data-ttu-id="37be6-332">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="37be6-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37be6-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-333">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-334">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="37be6-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="37be6-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37be6-335">Az.MachineLearning</span></span>
* <span data-ttu-id="37be6-336">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="37be6-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="37be6-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37be6-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="37be6-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="37be6-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="37be6-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37be6-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="37be6-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37be6-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="37be6-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="37be6-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="37be6-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="37be6-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="37be6-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="37be6-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-344">Az.Network</span></span>
* <span data-ttu-id="37be6-345">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="37be6-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-347">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="37be6-348">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="37be6-349">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="37be6-350">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-351">Az.Resources</span></span>
* <span data-ttu-id="37be6-352">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="37be6-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-353">Az.Sql</span></span>
* <span data-ttu-id="37be6-354">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="37be6-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="37be6-355">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="37be6-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="37be6-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="37be6-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="37be6-357">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="37be6-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-358">Az.Storage</span></span>
* <span data-ttu-id="37be6-359">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="37be6-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="37be6-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="37be6-361">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="37be6-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="37be6-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="37be6-363">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="37be6-364">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-364">General</span></span>
* <span data-ttu-id="37be6-365">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="37be6-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-366">Az.Accounts</span></span>
* <span data-ttu-id="37be6-367">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="37be6-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="37be6-368">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="37be6-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37be6-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-369">Az.Batch</span></span>
* <span data-ttu-id="37be6-370">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="37be6-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-371">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-372">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="37be6-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-373">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-374">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="37be6-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="37be6-375">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="37be6-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37be6-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37be6-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="37be6-377">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="37be6-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-378">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-379">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="37be6-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="37be6-380">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="37be6-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="37be6-381">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="37be6-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-382">Az.Monitor</span></span>
* <span data-ttu-id="37be6-383">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="37be6-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="37be6-384">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="37be6-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="37be6-385">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="37be6-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-386">Az.Network</span></span>
* <span data-ttu-id="37be6-387">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="37be6-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-388">Az.Resources</span></span>
* <span data-ttu-id="37be6-389">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="37be6-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="37be6-390">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="37be6-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-391">Az.Sql</span></span>
* <span data-ttu-id="37be6-392">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="37be6-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-393">Az.Storage</span></span>
* <span data-ttu-id="37be6-394">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="37be6-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="37be6-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="37be6-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="37be6-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="37be6-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="37be6-397">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="37be6-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="37be6-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="37be6-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="37be6-399">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="37be6-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="37be6-400">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="37be6-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="37be6-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="37be6-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="37be6-403">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="37be6-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="37be6-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="37be6-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="37be6-405">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="37be6-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="37be6-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="37be6-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="37be6-407">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-408">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-408">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-409">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="37be6-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="37be6-410">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="37be6-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-411">Az.Compute</span></span>
* <span data-ttu-id="37be6-412">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="37be6-412">VM Reapply feature</span></span>
    - <span data-ttu-id="37be6-413">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="37be6-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="37be6-414">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="37be6-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="37be6-415">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="37be6-416">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="37be6-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="37be6-417">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="37be6-418">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="37be6-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="37be6-419">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="37be6-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="37be6-420">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="37be6-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="37be6-421">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="37be6-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="37be6-422">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="37be6-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="37be6-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="37be6-424">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37be6-425">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="37be6-425">Get the Order</span></span>
* <span data-ttu-id="37be6-426">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37be6-427">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="37be6-427">Create new Order</span></span>
* <span data-ttu-id="37be6-428">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="37be6-429">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="37be6-429">Remove the Order</span></span>
* <span data-ttu-id="37be6-430">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="37be6-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="37be6-431">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="37be6-431">Now creates Local Share</span></span>
* <span data-ttu-id="37be6-432">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="37be6-433">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="37be6-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="37be6-434">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="37be6-435">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="37be6-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="37be6-436">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37be6-437">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="37be6-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="37be6-438">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37be6-439">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="37be6-439">Create new Triggers</span></span>
* <span data-ttu-id="37be6-440">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="37be6-441">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="37be6-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-442">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-443">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="37be6-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="37be6-444">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="37be6-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-446">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="37be6-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-447">Az.EventHub</span></span>
* <span data-ttu-id="37be6-448">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="37be6-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-449">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-450">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="37be6-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="37be6-451">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="37be6-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="37be6-452">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="37be6-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="37be6-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="37be6-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-454">Az.Network</span></span>
* <span data-ttu-id="37be6-455">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="37be6-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="37be6-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="37be6-456">Az.PrivateDns</span></span>
* <span data-ttu-id="37be6-457">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="37be6-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-459">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="37be6-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="37be6-460">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="37be6-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="37be6-461">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="37be6-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37be6-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37be6-462">Az.RedisCache</span></span>
* <span data-ttu-id="37be6-463">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="37be6-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="37be6-464">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="37be6-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="37be6-465">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="37be6-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-466">Az.Resources</span></span>
- <span data-ttu-id="37be6-467">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="37be6-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="37be6-468">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="37be6-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="37be6-469">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="37be6-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="37be6-470">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="37be6-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="37be6-471">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="37be6-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-472">Az.Sql</span></span>
* <span data-ttu-id="37be6-473">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="37be6-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="37be6-474">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="37be6-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="37be6-475">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="37be6-476">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-476">General</span></span>
* <span data-ttu-id="37be6-477">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="37be6-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-478">Az.Accounts</span></span>
* <span data-ttu-id="37be6-479">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="37be6-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="37be6-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37be6-480">Az.Advisor</span></span>
* <span data-ttu-id="37be6-481">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37be6-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37be6-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-482">Az.Batch</span></span>
* <span data-ttu-id="37be6-483">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="37be6-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="37be6-484">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="37be6-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="37be6-485">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="37be6-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="37be6-486">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="37be6-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="37be6-487">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="37be6-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="37be6-488">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="37be6-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="37be6-489">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="37be6-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="37be6-490">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="37be6-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="37be6-491">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="37be6-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="37be6-492">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="37be6-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="37be6-493">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="37be6-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="37be6-494">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="37be6-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="37be6-495">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="37be6-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="37be6-496">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="37be6-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="37be6-497">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="37be6-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="37be6-498">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="37be6-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="37be6-499">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="37be6-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="37be6-500">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="37be6-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="37be6-501">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="37be6-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="37be6-502">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="37be6-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="37be6-503">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="37be6-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="37be6-504">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="37be6-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="37be6-505">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="37be6-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="37be6-506">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="37be6-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="37be6-507">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="37be6-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="37be6-508">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="37be6-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="37be6-509">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="37be6-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="37be6-510">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="37be6-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="37be6-511">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="37be6-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="37be6-512">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="37be6-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="37be6-513">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="37be6-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="37be6-514">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="37be6-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="37be6-515">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="37be6-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="37be6-516">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="37be6-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="37be6-517">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="37be6-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="37be6-518">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="37be6-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-519">Az.Cdn</span></span>
* <span data-ttu-id="37be6-520">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="37be6-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="37be6-521">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="37be6-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-522">Az.Compute</span></span>
* <span data-ttu-id="37be6-523">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="37be6-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="37be6-524">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="37be6-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="37be6-525">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="37be6-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="37be6-526">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37be6-527">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="37be6-528">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="37be6-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="37be6-529">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="37be6-530">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="37be6-530">Breaking changes</span></span>
    - <span data-ttu-id="37be6-531">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="37be6-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="37be6-532">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="37be6-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-533">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-534">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="37be6-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-536">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="37be6-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="37be6-537">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="37be6-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="37be6-538">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="37be6-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="37be6-539">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="37be6-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="37be6-540">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="37be6-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="37be6-541">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="37be6-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-542">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-543">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="37be6-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37be6-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-544">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-545">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="37be6-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="37be6-546">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="37be6-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="37be6-547">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="37be6-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="37be6-548">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="37be6-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="37be6-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37be6-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37be6-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37be6-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37be6-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="37be6-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="37be6-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37be6-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="37be6-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37be6-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="37be6-554">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="37be6-555">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="37be6-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="37be6-556">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="37be6-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="37be6-557">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="37be6-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="37be6-558">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="37be6-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="37be6-559">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="37be6-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="37be6-560">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="37be6-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="37be6-561">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="37be6-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="37be6-562">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="37be6-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="37be6-563">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="37be6-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="37be6-564">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="37be6-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="37be6-565">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="37be6-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="37be6-566">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="37be6-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-567">Az.IotHub</span></span>
* <span data-ttu-id="37be6-568">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="37be6-568">Breaking changes:</span></span>
    - <span data-ttu-id="37be6-569">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="37be6-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37be6-570">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="37be6-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37be6-571">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="37be6-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37be6-572">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="37be6-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37be6-573">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="37be6-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="37be6-574">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="37be6-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="37be6-575">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="37be6-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="37be6-576">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="37be6-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="37be6-577">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="37be6-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37be6-578">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="37be6-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="37be6-579">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="37be6-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="37be6-580">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="37be6-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-582">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-583">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="37be6-584">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="37be6-585">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-586">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-587">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-588">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-589">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-590">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="37be6-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-591">Az.Resources</span></span>
* <span data-ttu-id="37be6-592">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="37be6-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-593">Az.Network</span></span>
* <span data-ttu-id="37be6-594">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="37be6-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="37be6-595">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="37be6-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="37be6-601">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="37be6-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="37be6-602">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-602">New cmdlet:</span></span>
        - <span data-ttu-id="37be6-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="37be6-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="37be6-604">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="37be6-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="37be6-605">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="37be6-606">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="37be6-607">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="37be6-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="37be6-608">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="37be6-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="37be6-609">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="37be6-610">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="37be6-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="37be6-611">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-611">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="37be6-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="37be6-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37be6-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37be6-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="37be6-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="37be6-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="37be6-617">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="37be6-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="37be6-618">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="37be6-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37be6-619">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="37be6-620">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="37be6-621">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="37be6-622">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="37be6-623">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="37be6-624">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-624">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="37be6-626">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="37be6-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37be6-627">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37be6-628">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37be6-629">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37be6-630">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="37be6-631">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="37be6-632">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="37be6-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="37be6-633">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-633">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="37be6-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="37be6-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="37be6-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="37be6-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="37be6-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="37be6-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="37be6-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="37be6-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="37be6-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="37be6-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="37be6-640">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="37be6-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37be6-641">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="37be6-642">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="37be6-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="37be6-643">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="37be6-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="37be6-644">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="37be6-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="37be6-645">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="37be6-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="37be6-646">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="37be6-647">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="37be6-648">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="37be6-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="37be6-649">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="37be6-650">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="37be6-651">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-651">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="37be6-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="37be6-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="37be6-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-657">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="37be6-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-658">Az.Sql</span></span>
* <span data-ttu-id="37be6-659">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="37be6-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="37be6-660">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="37be6-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="37be6-661">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="37be6-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="37be6-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="37be6-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="37be6-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="37be6-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="37be6-664">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="37be6-665">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="37be6-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="37be6-666">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="37be6-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="37be6-667">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37be6-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-668">Az.Storage</span></span>
* <span data-ttu-id="37be6-669">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37be6-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="37be6-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="37be6-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="37be6-672">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="37be6-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="37be6-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37be6-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="37be6-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37be6-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="37be6-675">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="37be6-676">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-676">General</span></span>
* <span data-ttu-id="37be6-677">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="37be6-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-678">Az.Accounts</span></span>
* <span data-ttu-id="37be6-679">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="37be6-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37be6-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-680">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-681">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="37be6-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="37be6-682">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="37be6-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-683">Az.Automation</span></span>
* <span data-ttu-id="37be6-684">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="37be6-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37be6-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-685">Az.Batch</span></span>
* <span data-ttu-id="37be6-686">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="37be6-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-687">Az.Compute</span></span>
* <span data-ttu-id="37be6-688">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="37be6-689">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="37be6-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="37be6-690">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="37be6-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="37be6-691">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="37be6-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-692">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-693">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="37be6-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="37be6-694">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="37be6-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="37be6-695">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="37be6-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-697">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="37be6-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="37be6-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="37be6-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="37be6-699">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="37be6-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="37be6-700">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="37be6-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="37be6-701">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="37be6-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="37be6-702">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="37be6-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-703">Az.IotHub</span></span>
* <span data-ttu-id="37be6-704">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="37be6-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="37be6-705">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="37be6-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-706">Az.Monitor</span></span>
* <span data-ttu-id="37be6-707">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="37be6-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="37be6-708">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="37be6-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="37be6-709">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="37be6-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="37be6-710">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37be6-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-711">Az.Network</span></span>
* <span data-ttu-id="37be6-712">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="37be6-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="37be6-713">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="37be6-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="37be6-714">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-714">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="37be6-716">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="37be6-717">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="37be6-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="37be6-718">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="37be6-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="37be6-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37be6-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37be6-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="37be6-722">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="37be6-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="37be6-723">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="37be6-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="37be6-724">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="37be6-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="37be6-725">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="37be6-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37be6-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37be6-726">Az.RedisCache</span></span>
* <span data-ttu-id="37be6-727">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="37be6-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-728">Az.Sql</span></span>
* <span data-ttu-id="37be6-729">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="37be6-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-730">Az.Storage</span></span>
* <span data-ttu-id="37be6-731">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="37be6-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="37be6-732">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="37be6-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="37be6-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37be6-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="37be6-734">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="37be6-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="37be6-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37be6-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37be6-736">Az.StorageSync</span></span>
* <span data-ttu-id="37be6-737">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="37be6-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-738">Az.Websites</span></span>
* <span data-ttu-id="37be6-739">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="37be6-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="37be6-740">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="37be6-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-741">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-742">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="37be6-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="37be6-743">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="37be6-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="37be6-744">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="37be6-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-745">Az.Automation</span></span>
* <span data-ttu-id="37be6-746">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="37be6-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="37be6-747">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="37be6-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="37be6-748">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="37be6-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-749">Az.Compute</span></span>
* <span data-ttu-id="37be6-750">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="37be6-751">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37be6-752">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="37be6-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="37be6-753">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="37be6-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="37be6-754">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="37be6-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="37be6-755">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="37be6-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="37be6-756">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="37be6-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="37be6-757">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="37be6-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="37be6-758">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="37be6-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-759">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-760">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="37be6-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="37be6-761">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="37be6-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37be6-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-762">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-763">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="37be6-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-764">Az.IotHub</span></span>
* <span data-ttu-id="37be6-765">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="37be6-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="37be6-766">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="37be6-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="37be6-767">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="37be6-767">New cmdlets are:</span></span>
    - <span data-ttu-id="37be6-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37be6-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37be6-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37be6-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37be6-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37be6-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="37be6-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="37be6-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-772">Az.Monitor</span></span>
* <span data-ttu-id="37be6-773">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="37be6-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="37be6-774">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="37be6-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="37be6-775">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="37be6-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="37be6-776">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="37be6-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="37be6-777">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="37be6-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="37be6-778">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="37be6-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="37be6-779">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37be6-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="37be6-780">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="37be6-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="37be6-781">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="37be6-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="37be6-782">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="37be6-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="37be6-783">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="37be6-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="37be6-784">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="37be6-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="37be6-785">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="37be6-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="37be6-786">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="37be6-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="37be6-787">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="37be6-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="37be6-788">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="37be6-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="37be6-789">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="37be6-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="37be6-790">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="37be6-791">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="37be6-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="37be6-792">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-792">Overall improved help files</span></span>
* <span data-ttu-id="37be6-793">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="37be6-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-794">Az.Network</span></span>
* <span data-ttu-id="37be6-795">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="37be6-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="37be6-796">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="37be6-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="37be6-797">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="37be6-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="37be6-798">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="37be6-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="37be6-799">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="37be6-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="37be6-800">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="37be6-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="37be6-801">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="37be6-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="37be6-802">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="37be6-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="37be6-803">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="37be6-804">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="37be6-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="37be6-805">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="37be6-806">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="37be6-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="37be6-807">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-807">New cmdlets</span></span>
        - <span data-ttu-id="37be6-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="37be6-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="37be6-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="37be6-810">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="37be6-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="37be6-811">New-VpnSite</span></span>
        - <span data-ttu-id="37be6-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="37be6-812">Update-VpnSite</span></span>
        - <span data-ttu-id="37be6-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-813">New-VpnConnection</span></span>
        - <span data-ttu-id="37be6-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-814">Update-VpnConnection</span></span>
* <span data-ttu-id="37be6-815">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="37be6-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-817">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="37be6-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="37be6-818">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="37be6-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-819">Az.Resources</span></span>
* <span data-ttu-id="37be6-820">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="37be6-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-822">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="37be6-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="37be6-823">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="37be6-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="37be6-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37be6-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37be6-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37be6-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37be6-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37be6-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37be6-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="37be6-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="37be6-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37be6-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37be6-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37be6-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37be6-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37be6-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37be6-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37be6-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37be6-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="37be6-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="37be6-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="37be6-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="37be6-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="37be6-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="37be6-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="37be6-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="37be6-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="37be6-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="37be6-837">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="37be6-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37be6-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37be6-838">Az.SignalR</span></span>
* <span data-ttu-id="37be6-839">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="37be6-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-840">Az.Sql</span></span>
* <span data-ttu-id="37be6-841">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="37be6-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="37be6-842">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="37be6-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="37be6-843">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="37be6-844">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="37be6-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="37be6-845">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="37be6-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-846">Az.Storage</span></span>
* <span data-ttu-id="37be6-847">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="37be6-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="37be6-848">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="37be6-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="37be6-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37be6-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="37be6-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37be6-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="37be6-851">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="37be6-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="37be6-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37be6-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="37be6-853">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="37be6-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="37be6-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37be6-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37be6-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="37be6-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="37be6-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-858">Az.Websites</span></span>
* <span data-ttu-id="37be6-859">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="37be6-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="37be6-860">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="37be6-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="37be6-861">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="37be6-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="37be6-862">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="37be6-863">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-863">General</span></span>
* <span data-ttu-id="37be6-864">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="37be6-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-865">Az.Accounts</span></span>
* <span data-ttu-id="37be6-866">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="37be6-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="37be6-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37be6-867">Az.Aks</span></span>
* <span data-ttu-id="37be6-868">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="37be6-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="37be6-869">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="37be6-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37be6-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-870">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-871">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="37be6-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="37be6-872">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="37be6-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="37be6-873">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="37be6-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="37be6-874">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="37be6-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="37be6-875">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="37be6-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37be6-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-876">Az.Batch</span></span>
* <span data-ttu-id="37be6-877">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="37be6-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-878">Az.Cdn</span></span>
* <span data-ttu-id="37be6-879">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="37be6-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-880">Az.Compute</span></span>
* <span data-ttu-id="37be6-881">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="37be6-882">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="37be6-883">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="37be6-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="37be6-884">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="37be6-885">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="37be6-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="37be6-886">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="37be6-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="37be6-887">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="37be6-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="37be6-888">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="37be6-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-889">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-890">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="37be6-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="37be6-891">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="37be6-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="37be6-892">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="37be6-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="37be6-893">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="37be6-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-895">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="37be6-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-896">Az.EventHub</span></span>
* <span data-ttu-id="37be6-897">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="37be6-898">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="37be6-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="37be6-899">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="37be6-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="37be6-900">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="37be6-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="37be6-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="37be6-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="37be6-902">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="37be6-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-903">Az.Monitor</span></span>
* <span data-ttu-id="37be6-904">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-905">Az.Network</span></span>
* <span data-ttu-id="37be6-906">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="37be6-907">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="37be6-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="37be6-908">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="37be6-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="37be6-909">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="37be6-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="37be6-910">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="37be6-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="37be6-911">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="37be6-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="37be6-912">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="37be6-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-914">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="37be6-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="37be6-915">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="37be6-915">Added example</span></span>
    - <span data-ttu-id="37be6-916">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="37be6-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="37be6-917">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="37be6-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="37be6-918">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="37be6-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-920">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-921">Az.Resources</span></span>
* <span data-ttu-id="37be6-922">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="37be6-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="37be6-923">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="37be6-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="37be6-924">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="37be6-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="37be6-925">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-926">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-927">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="37be6-928">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="37be6-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="37be6-929">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="37be6-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-931">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="37be6-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="37be6-932">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="37be6-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="37be6-933">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="37be6-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="37be6-934">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="37be6-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="37be6-935">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="37be6-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="37be6-936">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="37be6-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-937">Az.Sql</span></span>
* <span data-ttu-id="37be6-938">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="37be6-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-939">Az.Storage</span></span>
* <span data-ttu-id="37be6-940">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="37be6-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="37be6-941">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="37be6-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="37be6-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37be6-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="37be6-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="37be6-944">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="37be6-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="37be6-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-946">Az.Websites</span></span>
* <span data-ttu-id="37be6-947">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37be6-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="37be6-948">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-949">Az.Accounts</span></span>
* <span data-ttu-id="37be6-950">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="37be6-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="37be6-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="37be6-952">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="37be6-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-953">Az.Automation</span></span>
* <span data-ttu-id="37be6-954">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="37be6-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-956">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="37be6-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-957">Az.Compute</span></span>
* <span data-ttu-id="37be6-958">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="37be6-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="37be6-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37be6-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="37be6-960">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="37be6-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="37be6-961">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="37be6-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-962">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-963">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="37be6-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="37be6-964">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="37be6-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-965">Az.EventHub</span></span>
* <span data-ttu-id="37be6-966">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="37be6-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="37be6-967">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="37be6-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-968">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-969">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="37be6-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37be6-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37be6-970">Az.LogicApp</span></span>
* <span data-ttu-id="37be6-971">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="37be6-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="37be6-972">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="37be6-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="37be6-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="37be6-973">Az.ManagedServices</span></span>
* <span data-ttu-id="37be6-974">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="37be6-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-975">Az.Network</span></span>
* <span data-ttu-id="37be6-976">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="37be6-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="37be6-977">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-977">New cmdlets</span></span>
        - <span data-ttu-id="37be6-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37be6-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37be6-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="37be6-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="37be6-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="37be6-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="37be6-986">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="37be6-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="37be6-987">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="37be6-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="37be6-988">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="37be6-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="37be6-989">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="37be6-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="37be6-990">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="37be6-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="37be6-991">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="37be6-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="37be6-992">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="37be6-992">Updated cmdlets</span></span>
        - <span data-ttu-id="37be6-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37be6-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="37be6-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="37be6-996">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="37be6-997">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="37be6-998">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="37be6-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="37be6-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="37be6-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="37be6-1002">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="37be6-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="37be6-1003">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="37be6-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="37be6-1004">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="37be6-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-1006">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="37be6-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="37be6-1007">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="37be6-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1009">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="37be6-1010">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="37be6-1011">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="37be6-1012">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="37be6-1013">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="37be6-1014">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="37be6-1015">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="37be6-1016">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="37be6-1017">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="37be6-1018">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="37be6-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1019">Az.Resources</span></span>
- <span data-ttu-id="37be6-1020">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="37be6-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="37be6-1021">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="37be6-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-1023">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="37be6-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="37be6-1024">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="37be6-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1025">Az.Sql</span></span>
* <span data-ttu-id="37be6-1026">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="37be6-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="37be6-1027">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="37be6-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="37be6-1028">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="37be6-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1029">Az.Storage</span></span>
* <span data-ttu-id="37be6-1030">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="37be6-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37be6-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37be6-1031">Az.StorageSync</span></span>
* <span data-ttu-id="37be6-1032">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="37be6-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="37be6-1033">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="37be6-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1034">Az.Websites</span></span>
* <span data-ttu-id="37be6-1035">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="37be6-1036">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="37be6-1037">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="37be6-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="37be6-1038">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1039">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1040">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="37be6-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="37be6-1041">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="37be6-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="37be6-1042">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="37be6-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="37be6-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37be6-1043">Az.Advisor</span></span>
* <span data-ttu-id="37be6-1044">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="37be6-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="37be6-1045">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="37be6-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="37be6-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-1047">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="37be6-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="37be6-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="37be6-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="37be6-1049">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="37be6-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="37be6-1050">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="37be6-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="37be6-1051">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="37be6-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="37be6-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="37be6-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="37be6-1053">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="37be6-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1054">Az.Automation</span></span>
* <span data-ttu-id="37be6-1055">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="37be6-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1056">Az.Compute</span></span>
* <span data-ttu-id="37be6-1057">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-1058">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-1059">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="37be6-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37be6-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37be6-1060">Az.EventGrid</span></span>
* <span data-ttu-id="37be6-1061">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="37be6-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1062">Az.IotHub</span></span>
* <span data-ttu-id="37be6-1063">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="37be6-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1064">Az.Network</span></span>
* <span data-ttu-id="37be6-1065">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="37be6-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="37be6-1066">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="37be6-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37be6-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="37be6-1068">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="37be6-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="37be6-1069">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="37be6-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-1071">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="37be6-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1073">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="37be6-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1074">Az.Resources</span></span>
    - <span data-ttu-id="37be6-1075">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="37be6-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="37be6-1076">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="37be6-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="37be6-1077">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="37be6-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="37be6-1078">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="37be6-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-1080">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="37be6-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1081">Az.Sql</span></span>
* <span data-ttu-id="37be6-1082">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="37be6-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="37be6-1083">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37be6-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="37be6-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37be6-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37be6-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="37be6-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="37be6-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="37be6-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="37be6-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="37be6-1090">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="37be6-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1091">Az.Storage</span></span>
* <span data-ttu-id="37be6-1092">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="37be6-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37be6-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="37be6-1094">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="37be6-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="37be6-1095">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="37be6-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="37be6-1096">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="37be6-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="37be6-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="37be6-1099">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="37be6-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="37be6-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37be6-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="37be6-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="37be6-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="37be6-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="37be6-1102">Az.StorageSync</span></span>
* <span data-ttu-id="37be6-1103">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="37be6-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="37be6-1104">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1105">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1106">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="37be6-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="37be6-1107">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="37be6-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="37be6-1108">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="37be6-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="37be6-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="37be6-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="37be6-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="37be6-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1111">Az.Compute</span></span>
* <span data-ttu-id="37be6-1112">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="37be6-1113">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="37be6-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="37be6-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="37be6-1114">Az.Dns</span></span>
* <span data-ttu-id="37be6-1115">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37be6-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37be6-1116">Az.EventGrid</span></span>
* <span data-ttu-id="37be6-1117">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="37be6-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="37be6-1118">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37be6-1118">New cmdlets:</span></span>
    - <span data-ttu-id="37be6-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37be6-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37be6-1120">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37be6-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37be6-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37be6-1122">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="37be6-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37be6-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="37be6-1124">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37be6-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="37be6-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="37be6-1126">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="37be6-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="37be6-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="37be6-1128">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="37be6-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="37be6-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="37be6-1130">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="37be6-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="37be6-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="37be6-1132">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="37be6-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="37be6-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="37be6-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="37be6-1134">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="37be6-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="37be6-1135">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="37be6-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="37be6-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="37be6-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="37be6-1137">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="37be6-1138">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="37be6-1139">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="37be6-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="37be6-1140">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="37be6-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="37be6-1141">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="37be6-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="37be6-1142">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="37be6-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="37be6-1143">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="37be6-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="37be6-1144">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="37be6-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="37be6-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="37be6-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="37be6-1146">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="37be6-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="37be6-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="37be6-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="37be6-1148">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="37be6-1149">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="37be6-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="37be6-1152">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="37be6-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="37be6-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="37be6-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="37be6-1154">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="37be6-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1155">Az.Network</span></span>
* <span data-ttu-id="37be6-1156">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="37be6-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="37be6-1157">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-1157">New cmdlets</span></span>
        - <span data-ttu-id="37be6-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="37be6-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="37be6-1159">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="37be6-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="37be6-1160">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-1160">New cmdlets</span></span>
        - <span data-ttu-id="37be6-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="37be6-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="37be6-1162">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="37be6-1163">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-1163">New cmdlets</span></span>
        - <span data-ttu-id="37be6-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37be6-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37be6-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37be6-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="37be6-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="37be6-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="37be6-1169">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="37be6-1170">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-1170">New cmdlets</span></span>
        - <span data-ttu-id="37be6-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37be6-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37be6-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="37be6-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="37be6-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="37be6-1175">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="37be6-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="37be6-1176">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="37be6-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="37be6-1177">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="37be6-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="37be6-1178">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="37be6-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="37be6-1179">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="37be6-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="37be6-1180">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37be6-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="37be6-1181">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="37be6-1182">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="37be6-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="37be6-1183">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="37be6-1184">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="37be6-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="37be6-1185">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="37be6-1186">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="37be6-1187">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="37be6-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="37be6-1188">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="37be6-1189">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="37be6-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="37be6-1190">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="37be6-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="37be6-1191">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="37be6-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="37be6-1192">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="37be6-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="37be6-1193">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="37be6-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="37be6-1194">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="37be6-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="37be6-1195">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="37be6-1196">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="37be6-1197">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-1199">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="37be6-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1200">Az.Resources</span></span>
* <span data-ttu-id="37be6-1201">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="37be6-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="37be6-1202">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="37be6-1203">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="37be6-1204">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="37be6-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-1206">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="37be6-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1207">Az.Sql</span></span>
* <span data-ttu-id="37be6-1208">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="37be6-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="37be6-1209">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="37be6-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="37be6-1210">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="37be6-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="37be6-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37be6-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37be6-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37be6-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37be6-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="37be6-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="37be6-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="37be6-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="37be6-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="37be6-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1216">Az.Storage</span></span>
* <span data-ttu-id="37be6-1217">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37be6-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="37be6-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="37be6-1219">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="37be6-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="37be6-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1221">Az.Websites</span></span>
* <span data-ttu-id="37be6-1222">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="37be6-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="37be6-1223">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="37be6-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="37be6-1224">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="37be6-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-1225">Az.Cdn</span></span>
* <span data-ttu-id="37be6-1226">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="37be6-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1227">Az.Compute</span></span>
* <span data-ttu-id="37be6-1228">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="37be6-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="37be6-1229">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="37be6-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1230">Az.EventHub</span></span>
* <span data-ttu-id="37be6-1231">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="37be6-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="37be6-1232">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37be6-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1233">Az.Network</span></span>
* <span data-ttu-id="37be6-1234">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="37be6-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="37be6-1235">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="37be6-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37be6-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="37be6-1237">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="37be6-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1239">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="37be6-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-1241">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37be6-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-1243">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="37be6-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="37be6-1244">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1245">Az.Sql</span></span>
* <span data-ttu-id="37be6-1246">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="37be6-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="37be6-1247">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="37be6-1248">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="37be6-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="37be6-1249">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="37be6-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1250">Az.Websites</span></span>
* <span data-ttu-id="37be6-1251">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="37be6-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="37be6-1252">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="37be6-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-1254">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="37be6-1255">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="37be6-1256">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="37be6-1257">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="37be6-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="37be6-1258">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="37be6-1259">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="37be6-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="37be6-1260">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="37be6-1261">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="37be6-1262">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="37be6-1263">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="37be6-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="37be6-1264">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="37be6-1265">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="37be6-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="37be6-1266">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="37be6-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="37be6-1267">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="37be6-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="37be6-1268">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="37be6-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="37be6-1269">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="37be6-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="37be6-1270">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="37be6-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="37be6-1271">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="37be6-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="37be6-1272">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="37be6-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="37be6-1273">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="37be6-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="37be6-1274">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="37be6-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="37be6-1275">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="37be6-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="37be6-1276">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="37be6-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="37be6-1277">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="37be6-1278">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="37be6-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="37be6-1279">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="37be6-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="37be6-1280">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="37be6-1281">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="37be6-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="37be6-1282">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="37be6-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="37be6-1283">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="37be6-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="37be6-1284">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="37be6-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="37be6-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="37be6-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="37be6-1286">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="37be6-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="37be6-1287">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="37be6-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37be6-1288">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="37be6-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="37be6-1289">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="37be6-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="37be6-1290">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="37be6-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="37be6-1291">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="37be6-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="37be6-1292">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="37be6-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="37be6-1293">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="37be6-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37be6-1294">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="37be6-1295">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37be6-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="37be6-1296">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="37be6-1297">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="37be6-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="37be6-1298">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="37be6-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="37be6-1299">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="37be6-1300">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37be6-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="37be6-1301">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="37be6-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="37be6-1302">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="37be6-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="37be6-1303">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="37be6-1304">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="37be6-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="37be6-1305">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="37be6-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="37be6-1306">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="37be6-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="37be6-1307">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="37be6-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="37be6-1308">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="37be6-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="37be6-1309">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="37be6-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="37be6-1310">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="37be6-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="37be6-1311">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="37be6-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="37be6-1312">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="37be6-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="37be6-1313">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="37be6-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="37be6-1314">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="37be6-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="37be6-1315">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="37be6-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="37be6-1316">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="37be6-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="37be6-1317">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="37be6-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="37be6-1318">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="37be6-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="37be6-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="37be6-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="37be6-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="37be6-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="37be6-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="37be6-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="37be6-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="37be6-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="37be6-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37be6-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="37be6-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="37be6-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="37be6-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="37be6-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="37be6-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="37be6-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="37be6-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="37be6-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="37be6-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="37be6-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="37be6-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="37be6-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="37be6-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1331">Az.Automation</span></span>
* <span data-ttu-id="37be6-1332">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="37be6-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="37be6-1333">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="37be6-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="37be6-1334">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="37be6-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="37be6-1335">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="37be6-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="37be6-1336">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="37be6-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="37be6-1337">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="37be6-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="37be6-1338">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="37be6-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1339">Az.Compute</span></span>
* <span data-ttu-id="37be6-1340">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="37be6-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="37be6-1341">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="37be6-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-1343">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-1344">Az.Monitor</span></span>
* <span data-ttu-id="37be6-1345">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1346">Az.Network</span></span>
* <span data-ttu-id="37be6-1347">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="37be6-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="37be6-1348">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="37be6-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="37be6-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="37be6-1350">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="37be6-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1351">Az.Resources</span></span>
* <span data-ttu-id="37be6-1352">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="37be6-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1353">Az.Sql</span></span>
* <span data-ttu-id="37be6-1354">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="37be6-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="37be6-1355">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1356">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1357">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="37be6-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-1359">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="37be6-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="37be6-1360">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="37be6-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1361">Az.Compute</span></span>
* <span data-ttu-id="37be6-1362">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="37be6-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="37be6-1363">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="37be6-1364">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="37be6-1365">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="37be6-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="37be6-1366">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="37be6-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="37be6-1367">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="37be6-1368">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="37be6-1368">Breaking changes</span></span>
    - <span data-ttu-id="37be6-1369">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="37be6-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="37be6-1370">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="37be6-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="37be6-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="37be6-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="37be6-1372">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="37be6-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="37be6-1373">Az.Dns</span></span>
* <span data-ttu-id="37be6-1374">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="37be6-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="37be6-1375">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="37be6-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="37be6-1376">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="37be6-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="37be6-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="37be6-1378">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="37be6-1379">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="37be6-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="37be6-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-1380">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-1381">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="37be6-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="37be6-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37be6-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="37be6-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37be6-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="37be6-1384">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="37be6-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="37be6-1385">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="37be6-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="37be6-1386">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="37be6-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="37be6-1387">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="37be6-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-1388">Az.Monitor</span></span>
* <span data-ttu-id="37be6-1389">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="37be6-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="37be6-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="37be6-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="37be6-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="37be6-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="37be6-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="37be6-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="37be6-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="37be6-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="37be6-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="37be6-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="37be6-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="37be6-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37be6-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37be6-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37be6-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37be6-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="37be6-1401">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="37be6-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="37be6-1402">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="37be6-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1403">Az.Network</span></span>
* <span data-ttu-id="37be6-1404">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="37be6-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="37be6-1405">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="37be6-1405">New cmdlets</span></span>
        - <span data-ttu-id="37be6-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="37be6-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="37be6-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="37be6-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="37be6-1410">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="37be6-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="37be6-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="37be6-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="37be6-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="37be6-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="37be6-1413">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="37be6-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="37be6-1414">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="37be6-1415">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="37be6-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37be6-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="37be6-1417">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="37be6-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="37be6-1418">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="37be6-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="37be6-1419">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="37be6-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1421">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37be6-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="37be6-1422">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37be6-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="37be6-1423">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37be6-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="37be6-1424">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="37be6-1425">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37be6-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="37be6-1426">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="37be6-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="37be6-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="37be6-1427">Az.Relay</span></span>
* <span data-ttu-id="37be6-1428">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="37be6-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-1430">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="37be6-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1431">Az.Storage</span></span>
* <span data-ttu-id="37be6-1432">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="37be6-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="37be6-1433">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="37be6-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="37be6-1434">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="37be6-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="37be6-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="37be6-1436">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="37be6-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="37be6-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="37be6-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="37be6-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1440">Az.Websites</span></span>
* <span data-ttu-id="37be6-1441">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="37be6-1442">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="37be6-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="37be6-1443">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-1444">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-1445">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="37be6-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="37be6-1446">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="37be6-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37be6-1447">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="37be6-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37be6-1448">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37be6-1449">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="37be6-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37be6-1450">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37be6-1451">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="37be6-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1452">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1453">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="37be6-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="37be6-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-1454">Az.Batch</span></span>
* <span data-ttu-id="37be6-1455">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-1456">Az.Cdn</span></span>
* <span data-ttu-id="37be6-1457">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-1459">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1460">Az.Compute</span></span>
* <span data-ttu-id="37be6-1461">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="37be6-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="37be6-1462">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1463">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="37be6-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-1464">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-1465">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="37be6-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-1467">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37be6-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37be6-1468">Az.EventGrid</span></span>
* <span data-ttu-id="37be6-1469">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="37be6-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1470">Az.EventHub</span></span>
* <span data-ttu-id="37be6-1471">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="37be6-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="37be6-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="37be6-1472">Az.HDInsight</span></span>
* <span data-ttu-id="37be6-1473">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1474">Az.IotHub</span></span>
* <span data-ttu-id="37be6-1475">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1476">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-1477">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1478">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="37be6-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="37be6-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37be6-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="37be6-1480">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="37be6-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="37be6-1481">Az.Media</span></span>
* <span data-ttu-id="37be6-1482">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-1483">Az.Monitor</span></span>
  * <span data-ttu-id="37be6-1484">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="37be6-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="37be6-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="37be6-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="37be6-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="37be6-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="37be6-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37be6-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="37be6-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37be6-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="37be6-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="37be6-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="37be6-1490">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="37be6-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1491">Az.Network</span></span>
* <span data-ttu-id="37be6-1492">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1493">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="37be6-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="37be6-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="37be6-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="37be6-1495">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-1497">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="37be6-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="37be6-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="37be6-1499">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1501">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1502">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="37be6-1503">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="37be6-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="37be6-1504">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="37be6-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37be6-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37be6-1505">Az.RedisCache</span></span>
* <span data-ttu-id="37be6-1506">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1507">Az.Resources</span></span>
* <span data-ttu-id="37be6-1508">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="37be6-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1509">Az.Sql</span></span>
* <span data-ttu-id="37be6-1510">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="37be6-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="37be6-1511">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1512">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="37be6-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="37be6-1513">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="37be6-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="37be6-1514">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="37be6-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="37be6-1515">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="37be6-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="37be6-1516">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="37be6-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1517">Az.Websites</span></span>
* <span data-ttu-id="37be6-1518">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="37be6-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="37be6-1519">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="37be6-1520">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="37be6-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="37be6-1521">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="37be6-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="37be6-1522">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-1523">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-1524">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="37be6-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="37be6-1525">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="37be6-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37be6-1526">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="37be6-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37be6-1527">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37be6-1528">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="37be6-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37be6-1529">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37be6-1530">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="37be6-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="37be6-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1531">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1532">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="37be6-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37be6-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="37be6-1534">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="37be6-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="37be6-1535">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="37be6-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1536">Az.Automation</span></span>
* <span data-ttu-id="37be6-1537">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="37be6-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="37be6-1538">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="37be6-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="37be6-1539">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1540">Az.Compute</span></span>
* <span data-ttu-id="37be6-1541">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="37be6-1542">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="37be6-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="37be6-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="37be6-1544">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="37be6-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-1545">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-1546">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="37be6-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="37be6-1547">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="37be6-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1548">Az.Resources</span></span>
* <span data-ttu-id="37be6-1549">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="37be6-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="37be6-1550">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="37be6-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="37be6-1551">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="37be6-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="37be6-1552">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="37be6-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="37be6-1553">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="37be6-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="37be6-1554">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="37be6-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1555">Az.Sql</span></span>
* <span data-ttu-id="37be6-1556">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="37be6-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1557">Az.Storage</span></span>
* <span data-ttu-id="37be6-1558">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="37be6-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="37be6-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="37be6-1560">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="37be6-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="37be6-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="37be6-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="37be6-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="37be6-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="37be6-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="37be6-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="37be6-1565">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="37be6-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="37be6-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37be6-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="37be6-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37be6-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="37be6-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37be6-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="37be6-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="37be6-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="37be6-1570">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="37be6-1571">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="37be6-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="37be6-1572">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="37be6-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="37be6-1573">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="37be6-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="37be6-1574">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="37be6-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="37be6-1575">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="37be6-1576">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="37be6-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37be6-1577">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="37be6-1578">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="37be6-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1579">Az.Automation</span></span>
* <span data-ttu-id="37be6-1580">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="37be6-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="37be6-1581">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="37be6-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="37be6-1582">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="37be6-1582">Pre-Post script</span></span>
    * <span data-ttu-id="37be6-1583">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="37be6-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1584">Az.Compute</span></span>
* <span data-ttu-id="37be6-1585">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="37be6-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="37be6-1586">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="37be6-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1587">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-1588">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1589">Az.Network</span></span>
* <span data-ttu-id="37be6-1590">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="37be6-1591">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="37be6-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1593">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="37be6-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="37be6-1594">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="37be6-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1595">Az.Resources</span></span>
* <span data-ttu-id="37be6-1596">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37be6-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="37be6-1597">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="37be6-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1598">Az.Sql</span></span>
* <span data-ttu-id="37be6-1599">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="37be6-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1600">Az.Storage</span></span>
* <span data-ttu-id="37be6-1601">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="37be6-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="37be6-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37be6-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37be6-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="37be6-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="37be6-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="37be6-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="37be6-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="37be6-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1608">Az.Websites</span></span>
* <span data-ttu-id="37be6-1609">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="37be6-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="37be6-1610">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1611">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1612">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="37be6-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="37be6-1613">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1614">Az.Automation</span></span>
* <span data-ttu-id="37be6-1615">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="37be6-1616">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="37be6-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="37be6-1617">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="37be6-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-1618">Az.Cdn</span></span>
* <span data-ttu-id="37be6-1619">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="37be6-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1620">Az.Compute</span></span>
* <span data-ttu-id="37be6-1621">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="37be6-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-1622">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-1623">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="37be6-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37be6-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1624">Az.LogicApp</span></span>
* <span data-ttu-id="37be6-1625">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="37be6-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1626">Az.Network</span></span>
* <span data-ttu-id="37be6-1627">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1629">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="37be6-1630">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="37be6-1630">SDK Update</span></span>
* <span data-ttu-id="37be6-1631">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="37be6-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="37be6-1632">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="37be6-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1633">Az.Resources</span></span>
* <span data-ttu-id="37be6-1634">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="37be6-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="37be6-1635">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="37be6-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="37be6-1636">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="37be6-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="37be6-1637">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="37be6-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="37be6-1638">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="37be6-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="37be6-1639">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="37be6-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1640">Az.Sql</span></span>
* <span data-ttu-id="37be6-1641">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="37be6-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="37be6-1642">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="37be6-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1643">Az.Storage</span></span>
* <span data-ttu-id="37be6-1644">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="37be6-1645">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="37be6-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="37be6-1647">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1648">Az.Automation</span></span>
* <span data-ttu-id="37be6-1649">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="37be6-1650">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="37be6-1651">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-1653">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="37be6-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1654">Az.Compute</span></span>
* <span data-ttu-id="37be6-1655">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="37be6-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="37be6-1656">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="37be6-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="37be6-1657">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="37be6-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="37be6-1658">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="37be6-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-1660">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="37be6-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="37be6-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1661">Az.EventHub</span></span>
* <span data-ttu-id="37be6-1662">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1663">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-1664">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37be6-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37be6-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1665">Az.LogicApp</span></span>
* <span data-ttu-id="37be6-1666">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="37be6-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="37be6-1667">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="37be6-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="37be6-1668">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="37be6-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="37be6-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37be6-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37be6-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37be6-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37be6-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37be6-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="37be6-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="37be6-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="37be6-1673">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="37be6-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="37be6-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37be6-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37be6-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="37be6-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="37be6-1678">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="37be6-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="37be6-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-1679">Az.Monitor</span></span>
* <span data-ttu-id="37be6-1680">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="37be6-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1681">Az.Network</span></span>
* <span data-ttu-id="37be6-1682">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="37be6-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="37be6-1684">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="37be6-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="37be6-1685">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="37be6-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="37be6-1686">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="37be6-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1687">Az.Resources</span></span>
* <span data-ttu-id="37be6-1688">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="37be6-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="37be6-1689">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="37be6-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="37be6-1690">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="37be6-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="37be6-1691">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="37be6-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1692">Az.Sql</span></span>
* <span data-ttu-id="37be6-1693">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="37be6-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="37be6-1694">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="37be6-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1695">Az.Websites</span></span>
* <span data-ttu-id="37be6-1696">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="37be6-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="37be6-1697">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1698">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1699">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="37be6-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37be6-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="37be6-1701">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="37be6-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1702">Az.Compute</span></span>
* <span data-ttu-id="37be6-1703">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="37be6-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="37be6-1704">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="37be6-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="37be6-1705">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="37be6-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="37be6-1707">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="37be6-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1708">Az.Resources</span></span>
* <span data-ttu-id="37be6-1709">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="37be6-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="37be6-1710">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="37be6-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="37be6-1711">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="37be6-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="37be6-1712">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="37be6-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1713">Az.Sql</span></span>
* <span data-ttu-id="37be6-1714">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="37be6-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="37be6-1715">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="37be6-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="37be6-1716">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="37be6-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="37be6-1717">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1718">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1719">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="37be6-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="37be6-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="37be6-1721">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="37be6-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="37be6-1723">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="37be6-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="37be6-1724">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1725">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1726">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="37be6-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="37be6-1727">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37be6-1728">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="37be6-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="37be6-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="37be6-1729">Az.Aks</span></span>
* <span data-ttu-id="37be6-1730">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="37be6-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1731">Az.Automation</span></span>
* <span data-ttu-id="37be6-1732">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="37be6-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="37be6-1733">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="37be6-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="37be6-1734">Az.Cdn</span></span>
* <span data-ttu-id="37be6-1735">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1736">Az.Compute</span></span>
* <span data-ttu-id="37be6-1737">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="37be6-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="37be6-1738">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="37be6-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="37be6-1739">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="37be6-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="37be6-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37be6-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="37be6-1741">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="37be6-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="37be6-1742">Az.DataFactory</span></span>
* <span data-ttu-id="37be6-1743">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="37be6-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-1745">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="37be6-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="37be6-1746">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="37be6-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="37be6-1747">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1748">Az.IotHub</span></span>
* <span data-ttu-id="37be6-1749">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="37be6-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="37be6-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1750">Az.KeyVault</span></span>
* <span data-ttu-id="37be6-1751">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1752">Az.Network</span></span>
* <span data-ttu-id="37be6-1753">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1754">Az.Resources</span></span>
* <span data-ttu-id="37be6-1755">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="37be6-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="37be6-1756">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="37be6-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="37be6-1757">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="37be6-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="37be6-1758">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="37be6-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="37be6-1759">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="37be6-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="37be6-1760">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="37be6-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="37be6-1761">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="37be6-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-1763">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="37be6-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="37be6-1764">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="37be6-1764">Fix some error messages.</span></span>
* <span data-ttu-id="37be6-1765">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="37be6-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="37be6-1766">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="37be6-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37be6-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37be6-1767">Az.SignalR</span></span>
* <span data-ttu-id="37be6-1768">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1769">Az.Sql</span></span>
* <span data-ttu-id="37be6-1770">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37be6-1771">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="37be6-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="37be6-1772">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="37be6-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="37be6-1773">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="37be6-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1774">Az.Storage</span></span>
* <span data-ttu-id="37be6-1775">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37be6-1776">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="37be6-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="37be6-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="37be6-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="37be6-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="37be6-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="37be6-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="37be6-1780">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1781">Az.Websites</span></span>
* <span data-ttu-id="37be6-1782">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="37be6-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="37be6-1783">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="37be6-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="37be6-1784">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="37be6-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="37be6-1785">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="37be6-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="37be6-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1786">Az.Accounts</span></span>
* <span data-ttu-id="37be6-1787">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="37be6-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1788">Az.Compute</span></span>
* <span data-ttu-id="37be6-1789">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="37be6-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="37be6-1790">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="37be6-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="37be6-1791">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-1793">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="37be6-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="37be6-1794">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="37be6-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="37be6-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="37be6-1795">Az.EventGrid</span></span>
* <span data-ttu-id="37be6-1796">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="37be6-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="37be6-1797">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="37be6-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="37be6-1798">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="37be6-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="37be6-1799">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="37be6-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="37be6-1800">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="37be6-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="37be6-1801">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="37be6-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="37be6-1802">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="37be6-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="37be6-1803">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="37be6-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="37be6-1804">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="37be6-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="37be6-1805">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="37be6-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="37be6-1806">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="37be6-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="37be6-1807">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="37be6-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="37be6-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1808">Az.IotHub</span></span>
* <span data-ttu-id="37be6-1809">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="37be6-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="37be6-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="37be6-1810">Az.LogicApp</span></span>
* <span data-ttu-id="37be6-1811">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="37be6-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1812">Az.Resources</span></span>
* <span data-ttu-id="37be6-1813">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="37be6-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="37be6-1814">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="37be6-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="37be6-1815">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37be6-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="37be6-1816">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="37be6-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="37be6-1817">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="37be6-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="37be6-1818">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="37be6-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="37be6-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="37be6-1819">Az.SignalR</span></span>
* <span data-ttu-id="37be6-1820">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1821">Az.Sql</span></span>
* <span data-ttu-id="37be6-1822">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="37be6-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="37be6-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1823">Az.Storage</span></span>
* <span data-ttu-id="37be6-1824">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="37be6-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="37be6-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="37be6-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="37be6-1826">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="37be6-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="37be6-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="37be6-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1828">Az.Websites</span></span>
* <span data-ttu-id="37be6-1829">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="37be6-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="37be6-1830">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="37be6-1831">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="37be6-1832">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-1832">General</span></span>

- <span data-ttu-id="37be6-1833">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="37be6-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="37be6-1834">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="37be6-1834">Online help for each module</span></span>
- <span data-ttu-id="37be6-1835">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="37be6-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="37be6-1836">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="37be6-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="37be6-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1837">Az.Accounts</span></span>
- <span data-ttu-id="37be6-1838">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37be6-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="37be6-1839">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="37be6-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="37be6-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="37be6-1841">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="37be6-1841">Fixes for #7002</span></span>
- <span data-ttu-id="37be6-1842">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="37be6-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="37be6-1843">Az.Batch</span></span>
- <span data-ttu-id="37be6-1844">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="37be6-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="37be6-1845">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="37be6-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="37be6-1846">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="37be6-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="37be6-1847">Az.Billing</span></span>
- <span data-ttu-id="37be6-1848">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="37be6-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="37be6-1850">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="37be6-1851">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="37be6-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="37be6-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="37be6-1853">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="37be6-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="37be6-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="37be6-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="37be6-1855">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="37be6-1857">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="37be6-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="37be6-1858">Az.Monitor</span></span>
- <span data-ttu-id="37be6-1859">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="37be6-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="37be6-1860">Az.KeyVault</span></span>
- <span data-ttu-id="37be6-1861">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="37be6-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="37be6-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="37be6-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="37be6-1863">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="37be6-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="37be6-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="37be6-1864">Az.Media</span></span>
- <span data-ttu-id="37be6-1865">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="37be6-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="37be6-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1866">Az.Network</span></span>
<span data-ttu-id="37be6-1867">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="37be6-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="37be6-1868">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="37be6-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="37be6-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="37be6-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="37be6-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="37be6-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="37be6-1877">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37be6-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="37be6-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37be6-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="37be6-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="37be6-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37be6-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="37be6-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="37be6-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="37be6-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="37be6-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="37be6-1884">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="37be6-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="37be6-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37be6-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="37be6-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37be6-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="37be6-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="37be6-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="37be6-1888">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="37be6-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="37be6-1889">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="37be6-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="37be6-1891">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="37be6-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37be6-1892">Az.Profile</span></span>
- <span data-ttu-id="37be6-1893">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="37be6-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="37be6-1895">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="37be6-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1896">Az.Resources</span></span>
- <span data-ttu-id="37be6-1897">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="37be6-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="37be6-1899">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="37be6-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="37be6-1900">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="37be6-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="37be6-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="37be6-1902">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="37be6-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="37be6-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1903">Az.Sql</span></span>
- <span data-ttu-id="37be6-1904">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="37be6-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="37be6-1905">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="37be6-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="37be6-1906">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="37be6-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1907">Az.Storage</span></span>
- <span data-ttu-id="37be6-1908">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="37be6-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1909">Az.Websites</span></span>
- <span data-ttu-id="37be6-1910">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="37be6-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="37be6-1911">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="37be6-1912">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-1912">General</span></span>

* <span data-ttu-id="37be6-1913">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="37be6-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="37be6-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1914">Az.Compute</span></span>

* <span data-ttu-id="37be6-1915">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="37be6-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="37be6-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="37be6-1917">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="37be6-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="37be6-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="37be6-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="37be6-1919">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="37be6-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="37be6-1920">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="37be6-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="37be6-1921">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="37be6-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="37be6-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="37be6-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="37be6-1923">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="37be6-1924">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="37be6-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="37be6-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1925">Az.Resources</span></span>

* <span data-ttu-id="37be6-1926">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="37be6-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="37be6-1927">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="37be6-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="37be6-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1928">Az.Sql</span></span>

* <span data-ttu-id="37be6-1929">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="37be6-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="37be6-1930">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="37be6-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="37be6-1931">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="37be6-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="37be6-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-1932">Az.Storage</span></span>

* <span data-ttu-id="37be6-1933">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="37be6-1934">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="37be6-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="37be6-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="37be6-1936">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="37be6-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="37be6-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37be6-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="37be6-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="37be6-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="37be6-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-1939">Az.Websites</span></span>

* <span data-ttu-id="37be6-1940">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="37be6-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="37be6-1941">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="37be6-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="37be6-1942">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="37be6-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="37be6-1943">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="37be6-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="37be6-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="37be6-1945">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="37be6-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="37be6-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="37be6-1946">Az.Automation</span></span>
* <span data-ttu-id="37be6-1947">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="37be6-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="37be6-1948">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="37be6-1949">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="37be6-1950">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="37be6-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="37be6-1951">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="37be6-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="37be6-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-1952">Az.Compute</span></span>
* <span data-ttu-id="37be6-1953">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="37be6-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="37be6-1954">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="37be6-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="37be6-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="37be6-1956">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="37be6-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="37be6-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="37be6-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="37be6-1958">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="37be6-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="37be6-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-1959">Az.Network</span></span>
* <span data-ttu-id="37be6-1960">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="37be6-1961">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="37be6-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="37be6-1962">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="37be6-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="37be6-1963">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="37be6-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="37be6-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="37be6-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="37be6-1965">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="37be6-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="37be6-1966">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="37be6-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="37be6-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="37be6-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="37be6-1968">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="37be6-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="37be6-1969">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="37be6-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="37be6-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="37be6-1970">Az.Relay</span></span>
* <span data-ttu-id="37be6-1971">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="37be6-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="37be6-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-1972">Az.Resources</span></span>
* <span data-ttu-id="37be6-1973">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="37be6-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="37be6-1974">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="37be6-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="37be6-1975">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="37be6-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="37be6-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-1977">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="37be6-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="37be6-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-1978">Az.Sql</span></span>
* <span data-ttu-id="37be6-1979">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="37be6-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="37be6-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37be6-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37be6-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37be6-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37be6-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="37be6-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37be6-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37be6-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37be6-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37be6-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37be6-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="37be6-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="37be6-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="37be6-1988">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="37be6-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="37be6-1989">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="37be6-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="37be6-1990">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="37be6-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="37be6-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="37be6-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="37be6-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="37be6-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="37be6-1993">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="37be6-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="37be6-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="37be6-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="37be6-1995">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37be6-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="37be6-1996">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="37be6-1997">Geral</span><span class="sxs-lookup"><span data-stu-id="37be6-1997">General</span></span>
* <span data-ttu-id="37be6-1998">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="37be6-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="37be6-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37be6-1999">Az.Profile</span></span>
* <span data-ttu-id="37be6-2000">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="37be6-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="37be6-2001">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="37be6-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="37be6-2002">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="37be6-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="37be6-2003">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="37be6-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="37be6-2004">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="37be6-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="37be6-2005">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="37be6-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="37be6-2006">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="37be6-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-2008">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="37be6-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-2009">Az.Compute</span></span>
* <span data-ttu-id="37be6-2010">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="37be6-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="37be6-2011">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="37be6-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="37be6-2012">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="37be6-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-2014">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="37be6-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="37be6-2015">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="37be6-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="37be6-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="37be6-2016">Az.Insights</span></span>
* <span data-ttu-id="37be6-2017">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="37be6-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="37be6-2018">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="37be6-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="37be6-2019">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="37be6-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="37be6-2020">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="37be6-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-2021">Az.Network</span></span>
* <span data-ttu-id="37be6-2022">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="37be6-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="37be6-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="37be6-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="37be6-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="37be6-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="37be6-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="37be6-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="37be6-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="37be6-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="37be6-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="37be6-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="37be6-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="37be6-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="37be6-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="37be6-2030">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="37be6-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-2031">Az.Resources</span></span>
* <span data-ttu-id="37be6-2032">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="37be6-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="37be6-2033">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="37be6-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="37be6-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="37be6-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="37be6-2035">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="37be6-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="37be6-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="37be6-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="37be6-2037">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="37be6-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="37be6-2038">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="37be6-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="37be6-2039">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="37be6-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="37be6-2040">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="37be6-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="37be6-2041">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="37be6-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="37be6-2042">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="37be6-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="37be6-2043">Az.Profile</span></span>
* <span data-ttu-id="37be6-2044">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="37be6-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="37be6-2045">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="37be6-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-2046">Az.Compute</span></span>
* <span data-ttu-id="37be6-2047">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="37be6-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="37be6-2048">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37be6-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="37be6-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="37be6-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="37be6-2050">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="37be6-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="37be6-2051">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37be6-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="37be6-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="37be6-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="37be6-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="37be6-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="37be6-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37be6-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-2055">Az.Network</span></span>
* <span data-ttu-id="37be6-2056">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="37be6-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="37be6-2057">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37be6-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-2058">Az.Resources</span></span>
* <span data-ttu-id="37be6-2059">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="37be6-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="37be6-2060">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="37be6-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="37be6-2061">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="37be6-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="37be6-2062">Azure.Storage</span></span>
* <span data-ttu-id="37be6-2063">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="37be6-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="37be6-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="37be6-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="37be6-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="37be6-2066">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="37be6-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="37be6-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="37be6-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="37be6-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="37be6-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="37be6-2069">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="37be6-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="37be6-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="37be6-2070">Az.Compute</span></span>
* <span data-ttu-id="37be6-2071">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="37be6-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="37be6-2072">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="37be6-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="37be6-2073">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="37be6-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="37be6-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="37be6-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="37be6-2075">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="37be6-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="37be6-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="37be6-2076">Az.Network</span></span>
* <span data-ttu-id="37be6-2077">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="37be6-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="37be6-2078">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="37be6-2078">new cmdlets added</span></span>
    - <span data-ttu-id="37be6-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37be6-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="37be6-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37be6-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="37be6-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37be6-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="37be6-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="37be6-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="37be6-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="37be6-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="37be6-2085">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="37be6-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="37be6-2086">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="37be6-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="37be6-2087">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="37be6-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="37be6-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="37be6-2088">Az.RedisCache</span></span>
* <span data-ttu-id="37be6-2089">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="37be6-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="37be6-2090">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="37be6-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="37be6-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="37be6-2091">Az.Resources</span></span>
* <span data-ttu-id="37be6-2092">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37be6-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="37be6-2093">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="37be6-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="37be6-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="37be6-2094">Az.Sql</span></span>
* <span data-ttu-id="37be6-2095">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="37be6-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="37be6-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="37be6-2096">Az.Websites</span></span>
* <span data-ttu-id="37be6-2097">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="37be6-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="37be6-2098">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="37be6-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="37be6-2099">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="37be6-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="37be6-2100">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="37be6-2100">Initial Release</span></span>
