---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036154"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="10bc5-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="10bc5-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="10bc5-104">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="10bc5-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-105">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-106">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="10bc5-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="10bc5-107">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="10bc5-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="10bc5-108">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="10bc5-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-109">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-110">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="10bc5-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="10bc5-111">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="10bc5-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="10bc5-112">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="10bc5-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="10bc5-113">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="10bc5-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-115">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="10bc5-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-116">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-117">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="10bc5-118">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="10bc5-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="10bc5-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="10bc5-123">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="10bc5-124">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="10bc5-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="10bc5-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="10bc5-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="10bc5-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="10bc5-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="10bc5-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="10bc5-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="10bc5-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="10bc5-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="10bc5-129">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="10bc5-130">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="10bc5-131">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="10bc5-132">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="10bc5-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="10bc5-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="10bc5-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="10bc5-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="10bc5-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="10bc5-135">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10bc5-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-136">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-137">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="10bc5-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-138">Az.Network</span></span>
* <span data-ttu-id="10bc5-139">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="10bc5-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="10bc5-140">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="10bc5-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="10bc5-141">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="10bc5-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="10bc5-142">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-143">Az.Resources</span></span>
* <span data-ttu-id="10bc5-144">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="10bc5-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="10bc5-145">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="10bc5-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="10bc5-146">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="10bc5-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="10bc5-147">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="10bc5-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="10bc5-148">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="10bc5-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="10bc5-149">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="10bc5-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="10bc5-150">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="10bc5-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="10bc5-151">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="10bc5-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="10bc5-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="10bc5-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="10bc5-155">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="10bc5-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="10bc5-157">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="10bc5-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-158">Az.Sql</span></span>
* <span data-ttu-id="10bc5-159">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="10bc5-160">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="10bc5-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="10bc5-161">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="10bc5-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="10bc5-162">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="10bc5-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="10bc5-163">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="10bc5-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="10bc5-164">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="10bc5-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="10bc5-165">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="10bc5-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="10bc5-166">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="10bc5-167">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-168">Az.Storage</span></span>
* <span data-ttu-id="10bc5-169">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="10bc5-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="10bc5-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="10bc5-171">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="10bc5-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="10bc5-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="10bc5-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="10bc5-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="10bc5-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-174">Az.Websites</span></span>
* <span data-ttu-id="10bc5-175">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="10bc5-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="10bc5-176">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="10bc5-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="10bc5-177">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="10bc5-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="10bc5-178">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="10bc5-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="10bc5-179">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="10bc5-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="10bc5-180">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="10bc5-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-181">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-181">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-182">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="10bc5-183">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="10bc5-184">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="10bc5-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-185">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-186">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="10bc5-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-187">Az.Automation</span></span>
* <span data-ttu-id="10bc5-188">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="10bc5-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-190">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="10bc5-191">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="10bc5-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-192">Az.Compute</span></span>
* <span data-ttu-id="10bc5-193">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="10bc5-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-194">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-195">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="10bc5-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-196">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-197">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="10bc5-198">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="10bc5-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="10bc5-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="10bc5-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="10bc5-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-203">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-204">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="10bc5-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-205">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-206">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="10bc5-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="10bc5-207">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="10bc5-208">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="10bc5-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-209">Az.Network</span></span>
* <span data-ttu-id="10bc5-210">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="10bc5-211">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="10bc5-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="10bc5-212">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="10bc5-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="10bc5-213">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="10bc5-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="10bc5-214">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-214">No new cmdlets are added.</span></span> <span data-ttu-id="10bc5-215">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="10bc5-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-217">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="10bc5-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-218">Az.Resources</span></span>
* <span data-ttu-id="10bc5-219">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="10bc5-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="10bc5-220">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="10bc5-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="10bc5-221">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="10bc5-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="10bc5-222">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="10bc5-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="10bc5-223">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="10bc5-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="10bc5-224">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="10bc5-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="10bc5-225">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="10bc5-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="10bc5-226">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-227">Az.Sql</span></span>
* <span data-ttu-id="10bc5-228">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="10bc5-229">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="10bc5-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="10bc5-230">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="10bc5-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="10bc5-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="10bc5-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="10bc5-232">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="10bc5-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10bc5-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10bc5-233">Az.StorageSync</span></span>
* <span data-ttu-id="10bc5-234">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="10bc5-235">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="10bc5-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-236">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-236">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-237">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="10bc5-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="10bc5-238">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-239">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-240">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="10bc5-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="10bc5-241">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="10bc5-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-242">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-243">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="10bc5-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="10bc5-244">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="10bc5-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="10bc5-245">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="10bc5-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="10bc5-246">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="10bc5-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-247">Az.Compute</span></span>
* <span data-ttu-id="10bc5-248">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="10bc5-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="10bc5-249">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="10bc5-250">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="10bc5-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="10bc5-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="10bc5-252">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="10bc5-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-253">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-254">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="10bc5-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="10bc5-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="10bc5-256">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="10bc5-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="10bc5-257">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="10bc5-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-258">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-259">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="10bc5-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-260">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-261">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="10bc5-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-262">Az.Network</span></span>
* <span data-ttu-id="10bc5-263">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="10bc5-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="10bc5-264">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="10bc5-265">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="10bc5-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="10bc5-266">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="10bc5-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="10bc5-267">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="10bc5-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="10bc5-268">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="10bc5-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="10bc5-269">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="10bc5-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="10bc5-270">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="10bc5-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="10bc5-271">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-271">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="10bc5-273">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="10bc5-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="10bc5-275">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="10bc5-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10bc5-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="10bc5-277">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="10bc5-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="10bc5-278">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="10bc5-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="10bc5-279">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="10bc5-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="10bc5-280">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="10bc5-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-282">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="10bc5-283">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="10bc5-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-284">Az.Resources</span></span>
* <span data-ttu-id="10bc5-285">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="10bc5-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="10bc5-286">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="10bc5-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-287">Az.Sql</span></span>
<span data-ttu-id="10bc5-288">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="10bc5-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-289">Az.Storage</span></span>
* <span data-ttu-id="10bc5-290">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="10bc5-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="10bc5-292">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="10bc5-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="10bc5-293">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-294">Az.Websites</span></span>
* <span data-ttu-id="10bc5-295">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="10bc5-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="10bc5-296">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="10bc5-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="10bc5-297">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="10bc5-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-298">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-299">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="10bc5-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-300">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-301">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-302">Az.Compute</span></span>
* <span data-ttu-id="10bc5-303">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="10bc5-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="10bc5-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="10bc5-305">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="10bc5-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="10bc5-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="10bc5-307">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="10bc5-308">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="10bc5-309">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="10bc5-310">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="10bc5-311">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="10bc5-312">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="10bc5-313">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="10bc5-314">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="10bc5-315">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="10bc5-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="10bc5-316">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="10bc5-317">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="10bc5-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="10bc5-318">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="10bc5-319">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="10bc5-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="10bc5-320">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="10bc5-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="10bc5-321">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="10bc5-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="10bc5-322">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="10bc5-323">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="10bc5-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="10bc5-324">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="10bc5-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-325">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-326">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10bc5-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="10bc5-327">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="10bc5-328">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="10bc5-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="10bc5-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="10bc5-330">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="10bc5-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-331">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-332">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="10bc5-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-333">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-334">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="10bc5-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="10bc5-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10bc5-335">Az.MachineLearning</span></span>
* <span data-ttu-id="10bc5-336">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="10bc5-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="10bc5-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="10bc5-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="10bc5-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="10bc5-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="10bc5-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="10bc5-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="10bc5-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="10bc5-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="10bc5-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="10bc5-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="10bc5-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="10bc5-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="10bc5-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-344">Az.Network</span></span>
* <span data-ttu-id="10bc5-345">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="10bc5-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-347">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="10bc5-348">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="10bc5-349">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="10bc5-350">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-351">Az.Resources</span></span>
* <span data-ttu-id="10bc5-352">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-353">Az.Sql</span></span>
* <span data-ttu-id="10bc5-354">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="10bc5-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="10bc5-355">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="10bc5-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="10bc5-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="10bc5-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="10bc5-357">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="10bc5-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-358">Az.Storage</span></span>
* <span data-ttu-id="10bc5-359">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="10bc5-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="10bc5-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="10bc5-361">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="10bc5-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="10bc5-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="10bc5-363">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="10bc5-364">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-364">General</span></span>
* <span data-ttu-id="10bc5-365">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="10bc5-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-366">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-367">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="10bc5-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="10bc5-368">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="10bc5-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10bc5-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-369">Az.Batch</span></span>
* <span data-ttu-id="10bc5-370">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="10bc5-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-371">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-372">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-373">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-374">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="10bc5-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="10bc5-375">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="10bc5-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="10bc5-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="10bc5-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="10bc5-377">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="10bc5-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-378">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-379">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="10bc5-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="10bc5-380">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="10bc5-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="10bc5-381">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="10bc5-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-382">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-383">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="10bc5-384">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="10bc5-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="10bc5-385">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="10bc5-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-386">Az.Network</span></span>
* <span data-ttu-id="10bc5-387">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="10bc5-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-388">Az.Resources</span></span>
* <span data-ttu-id="10bc5-389">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="10bc5-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="10bc5-390">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-391">Az.Sql</span></span>
* <span data-ttu-id="10bc5-392">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="10bc5-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-393">Az.Storage</span></span>
* <span data-ttu-id="10bc5-394">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="10bc5-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="10bc5-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="10bc5-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="10bc5-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="10bc5-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="10bc5-397">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="10bc5-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="10bc5-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="10bc5-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="10bc5-399">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="10bc5-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="10bc5-400">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="10bc5-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="10bc5-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="10bc5-403">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="10bc5-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="10bc5-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="10bc5-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="10bc5-405">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="10bc5-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="10bc5-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="10bc5-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="10bc5-407">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-408">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-408">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-409">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="10bc5-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="10bc5-410">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="10bc5-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-411">Az.Compute</span></span>
* <span data-ttu-id="10bc5-412">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="10bc5-412">VM Reapply feature</span></span>
    - <span data-ttu-id="10bc5-413">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="10bc5-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="10bc5-414">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="10bc5-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="10bc5-415">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="10bc5-416">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10bc5-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="10bc5-417">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="10bc5-418">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="10bc5-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="10bc5-419">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="10bc5-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="10bc5-420">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="10bc5-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="10bc5-421">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="10bc5-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="10bc5-422">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="10bc5-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="10bc5-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="10bc5-424">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10bc5-425">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="10bc5-425">Get the Order</span></span>
* <span data-ttu-id="10bc5-426">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10bc5-427">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="10bc5-427">Create new Order</span></span>
* <span data-ttu-id="10bc5-428">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10bc5-429">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="10bc5-429">Remove the Order</span></span>
* <span data-ttu-id="10bc5-430">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="10bc5-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="10bc5-431">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="10bc5-431">Now creates Local Share</span></span>
* <span data-ttu-id="10bc5-432">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="10bc5-433">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="10bc5-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="10bc5-434">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="10bc5-435">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="10bc5-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="10bc5-436">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10bc5-437">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="10bc5-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="10bc5-438">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10bc5-439">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="10bc5-439">Create new Triggers</span></span>
* <span data-ttu-id="10bc5-440">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10bc5-441">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="10bc5-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-442">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-443">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="10bc5-444">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-446">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="10bc5-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-447">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-448">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="10bc5-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-449">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-450">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="10bc5-451">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="10bc5-452">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="10bc5-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="10bc5-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-454">Az.Network</span></span>
* <span data-ttu-id="10bc5-455">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="10bc5-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="10bc5-456">Az.PrivateDns</span></span>
* <span data-ttu-id="10bc5-457">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-459">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="10bc5-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="10bc5-460">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="10bc5-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="10bc5-461">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10bc5-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10bc5-462">Az.RedisCache</span></span>
* <span data-ttu-id="10bc5-463">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="10bc5-464">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="10bc5-465">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="10bc5-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-466">Az.Resources</span></span>
- <span data-ttu-id="10bc5-467">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="10bc5-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="10bc5-468">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="10bc5-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="10bc5-469">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="10bc5-470">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="10bc5-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="10bc5-471">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-472">Az.Sql</span></span>
* <span data-ttu-id="10bc5-473">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="10bc5-474">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="10bc5-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="10bc5-475">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="10bc5-476">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-476">General</span></span>
* <span data-ttu-id="10bc5-477">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="10bc5-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-478">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-479">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="10bc5-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10bc5-480">Az.Advisor</span></span>
* <span data-ttu-id="10bc5-481">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10bc5-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10bc5-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-482">Az.Batch</span></span>
* <span data-ttu-id="10bc5-483">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="10bc5-484">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="10bc5-485">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="10bc5-486">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="10bc5-487">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="10bc5-488">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="10bc5-489">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="10bc5-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="10bc5-490">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="10bc5-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="10bc5-491">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="10bc5-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="10bc5-492">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="10bc5-493">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="10bc5-494">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="10bc5-495">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="10bc5-496">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="10bc5-497">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="10bc5-498">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="10bc5-499">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="10bc5-500">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="10bc5-501">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="10bc5-502">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="10bc5-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="10bc5-503">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="10bc5-504">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="10bc5-505">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="10bc5-506">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="10bc5-507">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="10bc5-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="10bc5-508">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="10bc5-509">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="10bc5-510">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="10bc5-511">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="10bc5-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="10bc5-512">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="10bc5-513">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="10bc5-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="10bc5-514">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="10bc5-515">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="10bc5-516">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="10bc5-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="10bc5-517">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="10bc5-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="10bc5-518">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="10bc5-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-519">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-520">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="10bc5-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="10bc5-521">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="10bc5-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-522">Az.Compute</span></span>
* <span data-ttu-id="10bc5-523">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="10bc5-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="10bc5-524">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="10bc5-525">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="10bc5-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="10bc5-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="10bc5-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="10bc5-527">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10bc5-528">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="10bc5-529">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="10bc5-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="10bc5-530">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="10bc5-531">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="10bc5-531">Breaking changes</span></span>
    - <span data-ttu-id="10bc5-532">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="10bc5-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="10bc5-533">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="10bc5-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-534">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-535">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-537">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="10bc5-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="10bc5-538">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="10bc5-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="10bc5-539">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="10bc5-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="10bc5-540">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="10bc5-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="10bc5-541">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="10bc5-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="10bc5-542">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="10bc5-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-543">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-544">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="10bc5-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-545">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-546">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="10bc5-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="10bc5-547">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="10bc5-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="10bc5-548">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="10bc5-549">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="10bc5-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="10bc5-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10bc5-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10bc5-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10bc5-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10bc5-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10bc5-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10bc5-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10bc5-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="10bc5-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10bc5-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="10bc5-555">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="10bc5-556">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10bc5-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="10bc5-557">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10bc5-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="10bc5-558">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10bc5-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="10bc5-559">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="10bc5-560">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="10bc5-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="10bc5-561">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="10bc5-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="10bc5-562">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="10bc5-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="10bc5-563">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="10bc5-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="10bc5-564">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="10bc5-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="10bc5-565">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="10bc5-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="10bc5-566">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="10bc5-567">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-568">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-569">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="10bc5-569">Breaking changes:</span></span>
    - <span data-ttu-id="10bc5-570">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="10bc5-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10bc5-571">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10bc5-572">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="10bc5-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10bc5-573">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10bc5-574">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="10bc5-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="10bc5-575">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="10bc5-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="10bc5-576">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="10bc5-577">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="10bc5-578">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="10bc5-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10bc5-579">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10bc5-580">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="10bc5-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10bc5-581">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-583">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-584">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="10bc5-585">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="10bc5-586">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-587">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-588">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-589">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-590">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-591">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="10bc5-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-592">Az.Resources</span></span>
* <span data-ttu-id="10bc5-593">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="10bc5-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-594">Az.Network</span></span>
* <span data-ttu-id="10bc5-595">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="10bc5-596">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="10bc5-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="10bc5-602">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="10bc5-603">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-603">New cmdlet:</span></span>
        - <span data-ttu-id="10bc5-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="10bc5-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="10bc5-605">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="10bc5-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="10bc5-606">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="10bc5-607">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="10bc5-608">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="10bc5-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="10bc5-609">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="10bc5-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="10bc5-610">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="10bc5-611">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="10bc5-612">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-612">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="10bc5-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="10bc5-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10bc5-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10bc5-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10bc5-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="10bc5-618">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="10bc5-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="10bc5-619">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="10bc5-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10bc5-620">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="10bc5-621">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="10bc5-622">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="10bc5-623">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="10bc5-624">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="10bc5-625">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-625">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="10bc5-627">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="10bc5-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10bc5-628">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10bc5-629">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10bc5-630">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10bc5-631">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10bc5-632">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="10bc5-633">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="10bc5-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="10bc5-634">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-634">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="10bc5-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="10bc5-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="10bc5-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="10bc5-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="10bc5-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="10bc5-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="10bc5-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="10bc5-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="10bc5-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="10bc5-641">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="10bc5-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10bc5-642">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="10bc5-643">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="10bc5-644">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="10bc5-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="10bc5-645">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="10bc5-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="10bc5-646">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="10bc5-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10bc5-647">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="10bc5-648">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="10bc5-649">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="10bc5-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="10bc5-650">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="10bc5-651">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="10bc5-652">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-652">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="10bc5-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="10bc5-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="10bc5-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-658">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="10bc5-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-659">Az.Sql</span></span>
* <span data-ttu-id="10bc5-660">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="10bc5-661">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="10bc5-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="10bc5-662">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="10bc5-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="10bc5-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="10bc5-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="10bc5-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="10bc5-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="10bc5-665">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="10bc5-666">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="10bc5-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="10bc5-667">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="10bc5-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="10bc5-668">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-669">Az.Storage</span></span>
* <span data-ttu-id="10bc5-670">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="10bc5-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="10bc5-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="10bc5-673">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="10bc5-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="10bc5-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10bc5-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="10bc5-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10bc5-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="10bc5-676">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="10bc5-677">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-677">General</span></span>
* <span data-ttu-id="10bc5-678">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-679">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-680">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="10bc5-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-681">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-682">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="10bc5-683">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="10bc5-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-684">Az.Automation</span></span>
* <span data-ttu-id="10bc5-685">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="10bc5-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="10bc5-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-686">Az.Batch</span></span>
* <span data-ttu-id="10bc5-687">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="10bc5-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-688">Az.Compute</span></span>
* <span data-ttu-id="10bc5-689">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="10bc5-690">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="10bc5-691">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="10bc5-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="10bc5-692">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="10bc5-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-693">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-694">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="10bc5-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="10bc5-695">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="10bc5-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="10bc5-696">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-698">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="10bc5-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="10bc5-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="10bc5-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="10bc5-700">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="10bc5-701">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="10bc5-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="10bc5-702">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="10bc5-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="10bc5-703">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-704">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-705">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="10bc5-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="10bc5-706">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="10bc5-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-707">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-708">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="10bc5-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="10bc5-709">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="10bc5-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="10bc5-710">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="10bc5-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="10bc5-711">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="10bc5-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-712">Az.Network</span></span>
* <span data-ttu-id="10bc5-713">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="10bc5-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="10bc5-714">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="10bc5-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="10bc5-715">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-715">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="10bc5-717">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10bc5-718">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="10bc5-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="10bc5-719">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="10bc5-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10bc5-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10bc5-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="10bc5-723">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="10bc5-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="10bc5-724">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="10bc5-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="10bc5-725">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="10bc5-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="10bc5-726">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="10bc5-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10bc5-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10bc5-727">Az.RedisCache</span></span>
* <span data-ttu-id="10bc5-728">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="10bc5-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-729">Az.Sql</span></span>
* <span data-ttu-id="10bc5-730">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="10bc5-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-731">Az.Storage</span></span>
* <span data-ttu-id="10bc5-732">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="10bc5-733">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="10bc5-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="10bc5-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="10bc5-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="10bc5-735">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="10bc5-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="10bc5-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10bc5-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10bc5-737">Az.StorageSync</span></span>
* <span data-ttu-id="10bc5-738">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="10bc5-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-739">Az.Websites</span></span>
* <span data-ttu-id="10bc5-740">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="10bc5-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="10bc5-741">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-742">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-743">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="10bc5-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="10bc5-744">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="10bc5-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="10bc5-745">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-746">Az.Automation</span></span>
* <span data-ttu-id="10bc5-747">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="10bc5-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="10bc5-748">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="10bc5-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="10bc5-749">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="10bc5-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-750">Az.Compute</span></span>
* <span data-ttu-id="10bc5-751">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="10bc5-752">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10bc5-753">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="10bc5-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="10bc5-754">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="10bc5-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="10bc5-755">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="10bc5-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="10bc5-756">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="10bc5-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="10bc5-757">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="10bc5-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="10bc5-758">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="10bc5-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="10bc5-759">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="10bc5-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-760">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-761">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="10bc5-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="10bc5-762">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="10bc5-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-763">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-764">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="10bc5-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-765">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-766">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="10bc5-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="10bc5-767">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="10bc5-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="10bc5-768">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="10bc5-768">New cmdlets are:</span></span>
    - <span data-ttu-id="10bc5-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10bc5-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10bc5-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10bc5-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10bc5-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10bc5-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10bc5-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10bc5-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-773">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-774">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="10bc5-775">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="10bc5-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="10bc5-776">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="10bc5-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="10bc5-777">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="10bc5-778">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="10bc5-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="10bc5-779">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="10bc5-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="10bc5-780">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="10bc5-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="10bc5-781">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="10bc5-782">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="10bc5-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="10bc5-783">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="10bc5-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="10bc5-784">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="10bc5-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="10bc5-785">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="10bc5-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="10bc5-786">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="10bc5-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="10bc5-787">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="10bc5-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="10bc5-788">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="10bc5-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="10bc5-789">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="10bc5-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="10bc5-790">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="10bc5-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="10bc5-791">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="10bc5-792">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="10bc5-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="10bc5-793">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-793">Overall improved help files</span></span>
* <span data-ttu-id="10bc5-794">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="10bc5-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-795">Az.Network</span></span>
* <span data-ttu-id="10bc5-796">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="10bc5-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="10bc5-797">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="10bc5-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="10bc5-798">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="10bc5-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="10bc5-799">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="10bc5-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="10bc5-800">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="10bc5-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="10bc5-801">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="10bc5-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="10bc5-802">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="10bc5-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="10bc5-803">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="10bc5-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="10bc5-804">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="10bc5-805">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="10bc5-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="10bc5-806">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="10bc5-807">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="10bc5-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="10bc5-808">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-808">New cmdlets</span></span>
        - <span data-ttu-id="10bc5-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="10bc5-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="10bc5-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="10bc5-811">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="10bc5-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="10bc5-812">New-VpnSite</span></span>
        - <span data-ttu-id="10bc5-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="10bc5-813">Update-VpnSite</span></span>
        - <span data-ttu-id="10bc5-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-814">New-VpnConnection</span></span>
        - <span data-ttu-id="10bc5-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-815">Update-VpnConnection</span></span>
* <span data-ttu-id="10bc5-816">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="10bc5-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-818">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="10bc5-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="10bc5-819">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="10bc5-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-820">Az.Resources</span></span>
* <span data-ttu-id="10bc5-821">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="10bc5-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-823">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="10bc5-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="10bc5-824">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="10bc5-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="10bc5-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10bc5-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10bc5-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10bc5-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10bc5-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10bc5-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10bc5-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="10bc5-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="10bc5-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10bc5-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10bc5-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10bc5-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10bc5-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10bc5-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10bc5-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10bc5-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10bc5-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="10bc5-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="10bc5-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10bc5-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10bc5-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10bc5-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10bc5-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10bc5-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10bc5-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="10bc5-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="10bc5-838">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="10bc5-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10bc5-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10bc5-839">Az.SignalR</span></span>
* <span data-ttu-id="10bc5-840">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="10bc5-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-841">Az.Sql</span></span>
* <span data-ttu-id="10bc5-842">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="10bc5-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="10bc5-843">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="10bc5-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="10bc5-844">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="10bc5-845">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="10bc5-846">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="10bc5-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-847">Az.Storage</span></span>
* <span data-ttu-id="10bc5-848">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="10bc5-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="10bc5-849">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="10bc5-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="10bc5-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="10bc5-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="10bc5-852">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="10bc5-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="10bc5-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="10bc5-854">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="10bc5-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10bc5-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10bc5-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10bc5-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-859">Az.Websites</span></span>
* <span data-ttu-id="10bc5-860">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="10bc5-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="10bc5-861">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="10bc5-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="10bc5-862">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="10bc5-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="10bc5-863">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="10bc5-864">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-864">General</span></span>
* <span data-ttu-id="10bc5-865">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="10bc5-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-866">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-867">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="10bc5-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="10bc5-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10bc5-868">Az.Aks</span></span>
* <span data-ttu-id="10bc5-869">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="10bc5-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="10bc5-870">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="10bc5-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-871">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-872">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="10bc5-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="10bc5-873">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="10bc5-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="10bc5-874">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="10bc5-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="10bc5-875">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="10bc5-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="10bc5-876">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10bc5-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-877">Az.Batch</span></span>
* <span data-ttu-id="10bc5-878">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="10bc5-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-879">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-880">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="10bc5-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-881">Az.Compute</span></span>
* <span data-ttu-id="10bc5-882">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="10bc5-883">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="10bc5-884">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="10bc5-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="10bc5-885">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="10bc5-886">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="10bc5-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="10bc5-887">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10bc5-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="10bc5-888">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="10bc5-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="10bc5-889">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="10bc5-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-890">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-891">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="10bc5-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="10bc5-892">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="10bc5-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="10bc5-893">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="10bc5-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="10bc5-894">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="10bc5-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-896">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-897">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-898">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="10bc5-899">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="10bc5-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="10bc5-900">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="10bc5-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="10bc5-901">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="10bc5-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="10bc5-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10bc5-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10bc5-903">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="10bc5-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-904">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-905">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-906">Az.Network</span></span>
* <span data-ttu-id="10bc5-907">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="10bc5-908">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="10bc5-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="10bc5-909">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="10bc5-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="10bc5-910">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="10bc5-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="10bc5-911">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="10bc5-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="10bc5-912">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="10bc5-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="10bc5-913">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="10bc5-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-915">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="10bc5-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="10bc5-916">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="10bc5-916">Added example</span></span>
    - <span data-ttu-id="10bc5-917">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="10bc5-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="10bc5-918">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10bc5-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="10bc5-919">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10bc5-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-921">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-922">Az.Resources</span></span>
* <span data-ttu-id="10bc5-923">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="10bc5-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="10bc5-924">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="10bc5-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="10bc5-925">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="10bc5-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="10bc5-926">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-927">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-928">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="10bc5-929">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="10bc5-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="10bc5-930">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="10bc5-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-932">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="10bc5-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="10bc5-933">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="10bc5-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="10bc5-934">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="10bc5-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="10bc5-935">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="10bc5-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="10bc5-936">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="10bc5-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="10bc5-937">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="10bc5-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-938">Az.Sql</span></span>
* <span data-ttu-id="10bc5-939">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="10bc5-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-940">Az.Storage</span></span>
* <span data-ttu-id="10bc5-941">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="10bc5-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="10bc5-942">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="10bc5-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="10bc5-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="10bc5-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="10bc5-945">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="10bc5-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="10bc5-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-947">Az.Websites</span></span>
* <span data-ttu-id="10bc5-948">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10bc5-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="10bc5-949">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-950">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-951">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10bc5-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="10bc5-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="10bc5-953">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="10bc5-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="10bc5-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-954">Az.Automation</span></span>
* <span data-ttu-id="10bc5-955">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="10bc5-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-957">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-958">Az.Compute</span></span>
* <span data-ttu-id="10bc5-959">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="10bc5-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10bc5-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10bc5-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10bc5-961">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="10bc5-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="10bc5-962">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="10bc5-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-963">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-964">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="10bc5-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="10bc5-965">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="10bc5-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-966">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-967">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10bc5-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10bc5-968">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="10bc5-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-969">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-970">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="10bc5-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10bc5-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-971">Az.LogicApp</span></span>
* <span data-ttu-id="10bc5-972">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="10bc5-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="10bc5-973">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="10bc5-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="10bc5-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-974">Az.ManagedServices</span></span>
* <span data-ttu-id="10bc5-975">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="10bc5-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-976">Az.Network</span></span>
* <span data-ttu-id="10bc5-977">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="10bc5-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="10bc5-978">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-978">New cmdlets</span></span>
        - <span data-ttu-id="10bc5-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10bc5-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10bc5-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10bc5-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="10bc5-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="10bc5-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="10bc5-987">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="10bc5-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="10bc5-988">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="10bc5-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="10bc5-989">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="10bc5-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="10bc5-990">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="10bc5-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="10bc5-991">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="10bc5-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="10bc5-992">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="10bc5-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="10bc5-993">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="10bc5-993">Updated cmdlets</span></span>
        - <span data-ttu-id="10bc5-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10bc5-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10bc5-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="10bc5-997">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10bc5-998">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="10bc5-999">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="10bc5-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10bc5-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10bc5-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="10bc5-1003">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="10bc5-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="10bc5-1004">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="10bc5-1005">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-1007">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="10bc5-1008">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="10bc5-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1010">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10bc5-1011">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="10bc5-1012">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="10bc5-1013">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10bc5-1014">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="10bc5-1015">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10bc5-1016">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="10bc5-1017">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10bc5-1018">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="10bc5-1019">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1020">Az.Resources</span></span>
- <span data-ttu-id="10bc5-1021">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="10bc5-1022">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10bc5-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-1024">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10bc5-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10bc5-1025">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="10bc5-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1026">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1027">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="10bc5-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="10bc5-1028">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="10bc5-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="10bc5-1029">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1030">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1031">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="10bc5-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10bc5-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10bc5-1032">Az.StorageSync</span></span>
* <span data-ttu-id="10bc5-1033">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="10bc5-1034">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="10bc5-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1035">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1036">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="10bc5-1037">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="10bc5-1038">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="10bc5-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="10bc5-1039">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1040">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1041">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="10bc5-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="10bc5-1042">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="10bc5-1043">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="10bc5-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="10bc5-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1044">Az.Advisor</span></span>
* <span data-ttu-id="10bc5-1045">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="10bc5-1046">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-1048">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="10bc5-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="10bc5-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="10bc5-1050">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="10bc5-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="10bc5-1051">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="10bc5-1052">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="10bc5-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="10bc5-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="10bc5-1054">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="10bc5-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1055">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1056">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1057">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1058">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-1059">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-1060">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10bc5-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10bc5-1061">Az.EventGrid</span></span>
* <span data-ttu-id="10bc5-1062">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1063">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-1064">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1065">Az.Network</span></span>
* <span data-ttu-id="10bc5-1066">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="10bc5-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="10bc5-1067">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10bc5-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="10bc5-1069">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="10bc5-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="10bc5-1070">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="10bc5-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-1072">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="10bc5-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1074">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="10bc5-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1075">Az.Resources</span></span>
    - <span data-ttu-id="10bc5-1076">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="10bc5-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="10bc5-1077">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="10bc5-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="10bc5-1078">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="10bc5-1079">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-1081">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1082">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1083">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="10bc5-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="10bc5-1084">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="10bc5-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10bc5-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10bc5-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10bc5-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10bc5-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10bc5-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="10bc5-1091">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="10bc5-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1092">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1093">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="10bc5-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10bc5-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="10bc5-1095">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="10bc5-1096">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="10bc5-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="10bc5-1097">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="10bc5-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="10bc5-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="10bc5-1100">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="10bc5-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10bc5-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="10bc5-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10bc5-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10bc5-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10bc5-1103">Az.StorageSync</span></span>
* <span data-ttu-id="10bc5-1104">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="10bc5-1105">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1106">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1107">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="10bc5-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="10bc5-1108">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="10bc5-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="10bc5-1109">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="10bc5-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="10bc5-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="10bc5-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="10bc5-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="10bc5-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1112">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1113">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="10bc5-1114">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="10bc5-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10bc5-1115">Az.Dns</span></span>
* <span data-ttu-id="10bc5-1116">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10bc5-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10bc5-1117">Az.EventGrid</span></span>
* <span data-ttu-id="10bc5-1118">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="10bc5-1119">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1119">New cmdlets:</span></span>
    - <span data-ttu-id="10bc5-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10bc5-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10bc5-1121">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10bc5-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10bc5-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10bc5-1123">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="10bc5-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10bc5-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10bc5-1125">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10bc5-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10bc5-1127">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10bc5-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10bc5-1129">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="10bc5-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10bc5-1131">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="10bc5-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="10bc5-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="10bc5-1133">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="10bc5-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="10bc5-1134">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10bc5-1135">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="10bc5-1136">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="10bc5-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="10bc5-1138">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10bc5-1139">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10bc5-1140">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="10bc5-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="10bc5-1141">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="10bc5-1142">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="10bc5-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="10bc5-1143">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="10bc5-1144">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="10bc5-1145">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="10bc5-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="10bc5-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="10bc5-1147">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="10bc5-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="10bc5-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="10bc5-1149">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="10bc5-1150">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="10bc5-1153">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="10bc5-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="10bc5-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="10bc5-1155">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="10bc5-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1156">Az.Network</span></span>
* <span data-ttu-id="10bc5-1157">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="10bc5-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="10bc5-1158">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-1158">New cmdlets</span></span>
        - <span data-ttu-id="10bc5-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="10bc5-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="10bc5-1160">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10bc5-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="10bc5-1161">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-1161">New cmdlets</span></span> 
        - <span data-ttu-id="10bc5-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10bc5-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="10bc5-1163">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="10bc5-1164">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-1164">New cmdlets</span></span> 
        - <span data-ttu-id="10bc5-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="10bc5-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10bc5-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10bc5-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10bc5-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="10bc5-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="10bc5-1170">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="10bc5-1171">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-1171">New cmdlets</span></span>
        - <span data-ttu-id="10bc5-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10bc5-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10bc5-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10bc5-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10bc5-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="10bc5-1176">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10bc5-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="10bc5-1177">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="10bc5-1178">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="10bc5-1179">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="10bc5-1180">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="10bc5-1181">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="10bc5-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="10bc5-1182">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="10bc5-1183">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="10bc5-1184">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="10bc5-1185">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="10bc5-1186">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="10bc5-1187">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="10bc5-1188">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="10bc5-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="10bc5-1189">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="10bc5-1190">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="10bc5-1191">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="10bc5-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="10bc5-1192">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="10bc5-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="10bc5-1193">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="10bc5-1194">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="10bc5-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="10bc5-1195">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="10bc5-1196">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10bc5-1197">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10bc5-1198">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-1200">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1201">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1202">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="10bc5-1203">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10bc5-1204">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10bc5-1205">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-1207">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1208">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1209">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="10bc5-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="10bc5-1210">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="10bc5-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="10bc5-1211">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="10bc5-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10bc5-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10bc5-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10bc5-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10bc5-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10bc5-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="10bc5-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10bc5-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1217">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1218">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="10bc5-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="10bc5-1220">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="10bc5-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="10bc5-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1222">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1223">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="10bc5-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="10bc5-1224">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="10bc5-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="10bc5-1225">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="10bc5-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-1226">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-1227">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1228">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1229">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="10bc5-1230">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="10bc5-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1231">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-1232">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="10bc5-1233">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bc5-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1234">Az.Network</span></span>
* <span data-ttu-id="10bc5-1235">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="10bc5-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="10bc5-1236">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="10bc5-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10bc5-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="10bc5-1238">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="10bc5-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1240">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="10bc5-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-1242">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bc5-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-1244">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="10bc5-1245">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1246">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1247">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="10bc5-1248">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="10bc5-1249">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="10bc5-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="10bc5-1250">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1251">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1252">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="10bc5-1253">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="10bc5-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-1255">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="10bc5-1256">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="10bc5-1257">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="10bc5-1258">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="10bc5-1259">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="10bc5-1260">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="10bc5-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="10bc5-1261">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="10bc5-1262">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="10bc5-1263">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="10bc5-1264">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="10bc5-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="10bc5-1265">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="10bc5-1266">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="10bc5-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="10bc5-1267">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="10bc5-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="10bc5-1268">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="10bc5-1269">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="10bc5-1270">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="10bc5-1271">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="10bc5-1272">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="10bc5-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="10bc5-1273">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="10bc5-1274">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="10bc5-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="10bc5-1275">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="10bc5-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="10bc5-1276">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="10bc5-1277">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="10bc5-1278">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="10bc5-1279">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="10bc5-1280">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="10bc5-1281">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="10bc5-1282">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="10bc5-1283">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="10bc5-1284">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="10bc5-1285">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="10bc5-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="10bc5-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="10bc5-1287">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="10bc5-1288">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10bc5-1289">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="10bc5-1290">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="10bc5-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="10bc5-1291">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="10bc5-1292">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="10bc5-1293">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="10bc5-1294">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="10bc5-1295">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10bc5-1296">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="10bc5-1297">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="10bc5-1298">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10bc5-1299">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10bc5-1300">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10bc5-1301">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="10bc5-1302">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10bc5-1303">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="10bc5-1304">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="10bc5-1305">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="10bc5-1306">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="10bc5-1307">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="10bc5-1308">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="10bc5-1309">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="10bc5-1310">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="10bc5-1311">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10bc5-1312">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10bc5-1313">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10bc5-1314">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10bc5-1315">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10bc5-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10bc5-1316">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10bc5-1317">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10bc5-1318">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10bc5-1319">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="10bc5-1320">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="10bc5-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="10bc5-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="10bc5-1322">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="10bc5-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="10bc5-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="10bc5-1324">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="10bc5-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="10bc5-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="10bc5-1326">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="10bc5-1327">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="10bc5-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="10bc5-1329">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="10bc5-1330">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="10bc5-1331">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1332">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1333">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="10bc5-1334">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="10bc5-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="10bc5-1335">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="10bc5-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="10bc5-1336">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="10bc5-1337">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="10bc5-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="10bc5-1338">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="10bc5-1339">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1340">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1341">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="10bc5-1342">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-1344">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1345">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-1346">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1347">Az.Network</span></span>
* <span data-ttu-id="10bc5-1348">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="10bc5-1349">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="10bc5-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="10bc5-1351">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10bc5-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1352">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1353">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="10bc5-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1354">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1355">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="10bc5-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="10bc5-1356">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1357">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1358">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="10bc5-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-1360">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="10bc5-1361">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1362">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1363">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="10bc5-1364">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="10bc5-1365">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="10bc5-1366">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="10bc5-1367">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="10bc5-1368">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="10bc5-1369">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="10bc5-1369">Breaking changes</span></span>
    - <span data-ttu-id="10bc5-1370">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="10bc5-1371">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="10bc5-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="10bc5-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="10bc5-1373">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="10bc5-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10bc5-1374">Az.Dns</span></span>
* <span data-ttu-id="10bc5-1375">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="10bc5-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="10bc5-1376">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="10bc5-1377">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="10bc5-1379">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="10bc5-1380">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-1381">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-1382">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="10bc5-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10bc5-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="10bc5-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10bc5-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10bc5-1385">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10bc5-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10bc5-1386">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="10bc5-1387">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="10bc5-1388">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1389">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-1390">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="10bc5-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="10bc5-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="10bc5-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="10bc5-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="10bc5-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="10bc5-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="10bc5-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="10bc5-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="10bc5-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="10bc5-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="10bc5-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="10bc5-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10bc5-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10bc5-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10bc5-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10bc5-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10bc5-1402">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="10bc5-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="10bc5-1403">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="10bc5-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1404">Az.Network</span></span>
* <span data-ttu-id="10bc5-1405">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="10bc5-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="10bc5-1406">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="10bc5-1406">New cmdlets</span></span>
        - <span data-ttu-id="10bc5-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="10bc5-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="10bc5-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="10bc5-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="10bc5-1411">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="10bc5-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10bc5-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="10bc5-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10bc5-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="10bc5-1414">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="10bc5-1415">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="10bc5-1416">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10bc5-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="10bc5-1418">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="10bc5-1419">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="10bc5-1420">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1422">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="10bc5-1423">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="10bc5-1424">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="10bc5-1425">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="10bc5-1426">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="10bc5-1427">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="10bc5-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10bc5-1428">Az.Relay</span></span>
* <span data-ttu-id="10bc5-1429">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="10bc5-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-1431">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="10bc5-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1432">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1433">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="10bc5-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="10bc5-1434">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="10bc5-1435">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="10bc5-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="10bc5-1437">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="10bc5-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="10bc5-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="10bc5-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1441">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1442">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="10bc5-1443">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="10bc5-1444">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-1445">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-1446">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="10bc5-1447">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10bc5-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10bc5-1448">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10bc5-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10bc5-1449">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10bc5-1450">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10bc5-1451">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10bc5-1452">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="10bc5-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1453">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1454">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="10bc5-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10bc5-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-1455">Az.Batch</span></span>
* <span data-ttu-id="10bc5-1456">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-1457">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-1458">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-1460">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1461">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1462">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="10bc5-1463">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1464">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="10bc5-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-1465">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-1466">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-1468">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10bc5-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10bc5-1469">Az.EventGrid</span></span>
* <span data-ttu-id="10bc5-1470">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1471">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-1472">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="10bc5-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="10bc5-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10bc5-1473">Az.HDInsight</span></span>
* <span data-ttu-id="10bc5-1474">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1475">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-1476">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1477">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-1478">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1479">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="10bc5-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="10bc5-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10bc5-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="10bc5-1481">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="10bc5-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10bc5-1482">Az.Media</span></span>
* <span data-ttu-id="10bc5-1483">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1484">Az.Monitor</span></span>
  * <span data-ttu-id="10bc5-1485">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="10bc5-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="10bc5-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="10bc5-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="10bc5-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="10bc5-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="10bc5-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10bc5-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10bc5-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10bc5-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10bc5-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10bc5-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="10bc5-1491">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="10bc5-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1492">Az.Network</span></span>
* <span data-ttu-id="10bc5-1493">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1494">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="10bc5-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="10bc5-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10bc5-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="10bc5-1496">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-1498">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="10bc5-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10bc5-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="10bc5-1500">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1502">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1503">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="10bc5-1504">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="10bc5-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="10bc5-1505">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="10bc5-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10bc5-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10bc5-1506">Az.RedisCache</span></span>
* <span data-ttu-id="10bc5-1507">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1508">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1509">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="10bc5-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1510">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1511">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="10bc5-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="10bc5-1512">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1513">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="10bc5-1514">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="10bc5-1515">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="10bc5-1516">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="10bc5-1517">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="10bc5-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1518">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1519">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="10bc5-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="10bc5-1520">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10bc5-1521">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="10bc5-1522">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="10bc5-1523">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-1524">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-1525">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="10bc5-1526">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10bc5-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10bc5-1527">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10bc5-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10bc5-1528">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10bc5-1529">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10bc5-1530">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10bc5-1531">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="10bc5-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1532">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1533">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="10bc5-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10bc5-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="10bc5-1535">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="10bc5-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="10bc5-1536">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="10bc5-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1537">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1538">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="10bc5-1539">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="10bc5-1540">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1541">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1542">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10bc5-1543">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="10bc5-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="10bc5-1545">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="10bc5-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-1546">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-1547">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="10bc5-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="10bc5-1548">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1549">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1550">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="10bc5-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="10bc5-1551">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="10bc5-1552">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="10bc5-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="10bc5-1553">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10bc5-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="10bc5-1554">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="10bc5-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="10bc5-1555">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10bc5-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1556">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1557">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1558">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1559">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="10bc5-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10bc5-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="10bc5-1561">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="10bc5-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10bc5-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10bc5-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10bc5-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10bc5-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="10bc5-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="10bc5-1566">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="10bc5-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10bc5-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10bc5-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="10bc5-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10bc5-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="10bc5-1571">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10bc5-1572">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="10bc5-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="10bc5-1573">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="10bc5-1574">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10bc5-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10bc5-1575">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10bc5-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10bc5-1576">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10bc5-1577">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10bc5-1578">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10bc5-1579">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="10bc5-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1580">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1581">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="10bc5-1582">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="10bc5-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="10bc5-1583">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="10bc5-1583">Pre-Post script</span></span>
    * <span data-ttu-id="10bc5-1584">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="10bc5-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1585">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1586">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="10bc5-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="10bc5-1587">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1588">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-1589">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1590">Az.Network</span></span>
* <span data-ttu-id="10bc5-1591">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="10bc5-1592">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1594">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="10bc5-1595">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="10bc5-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1596">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1597">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="10bc5-1598">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="10bc5-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1599">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1600">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1601">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1602">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="10bc5-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10bc5-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10bc5-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10bc5-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="10bc5-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="10bc5-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="10bc5-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="10bc5-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1609">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1610">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="10bc5-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="10bc5-1611">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1612">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1613">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="10bc5-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="10bc5-1614">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1615">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1616">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="10bc5-1617">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="10bc5-1618">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="10bc5-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-1619">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-1620">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1621">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1622">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="10bc5-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-1623">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-1624">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10bc5-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1625">Az.LogicApp</span></span>
* <span data-ttu-id="10bc5-1626">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1627">Az.Network</span></span>
* <span data-ttu-id="10bc5-1628">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1630">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="10bc5-1631">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="10bc5-1631">SDK Update</span></span>
* <span data-ttu-id="10bc5-1632">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10bc5-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="10bc5-1633">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10bc5-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1634">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1635">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="10bc5-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="10bc5-1636">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="10bc5-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="10bc5-1637">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="10bc5-1638">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="10bc5-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="10bc5-1639">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="10bc5-1640">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="10bc5-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1641">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1642">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="10bc5-1643">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1644">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1645">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="10bc5-1646">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="10bc5-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="10bc5-1648">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1649">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1650">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="10bc5-1651">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="10bc5-1652">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-1654">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1655">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1656">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="10bc5-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="10bc5-1657">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="10bc5-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="10bc5-1658">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="10bc5-1659">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-1661">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10bc5-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1662">Az.EventHub</span></span>
* <span data-ttu-id="10bc5-1663">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1664">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-1665">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="10bc5-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10bc5-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1666">Az.LogicApp</span></span>
* <span data-ttu-id="10bc5-1667">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="10bc5-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="10bc5-1668">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="10bc5-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="10bc5-1669">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="10bc5-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="10bc5-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10bc5-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10bc5-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10bc5-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10bc5-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10bc5-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10bc5-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10bc5-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="10bc5-1674">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="10bc5-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="10bc5-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10bc5-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10bc5-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10bc5-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="10bc5-1679">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10bc5-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1680">Az.Monitor</span></span>
* <span data-ttu-id="10bc5-1681">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1682">Az.Network</span></span>
* <span data-ttu-id="10bc5-1683">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="10bc5-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="10bc5-1685">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="10bc5-1686">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="10bc5-1687">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="10bc5-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1688">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1689">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10bc5-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10bc5-1690">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10bc5-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="10bc5-1691">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="10bc5-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="10bc5-1692">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="10bc5-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1693">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1694">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="10bc5-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="10bc5-1695">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="10bc5-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1696">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1697">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="10bc5-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="10bc5-1698">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1699">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1700">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10bc5-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10bc5-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="10bc5-1702">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1703">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1704">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="10bc5-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="10bc5-1705">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="10bc5-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="10bc5-1706">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="10bc5-1708">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1709">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1710">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="10bc5-1711">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10bc5-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10bc5-1712">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="10bc5-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="10bc5-1713">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10bc5-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1714">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1715">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="10bc5-1716">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="10bc5-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="10bc5-1717">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="10bc5-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="10bc5-1718">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1719">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1720">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="10bc5-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10bc5-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="10bc5-1722">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="10bc5-1724">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="10bc5-1725">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1726">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1727">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10bc5-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10bc5-1728">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10bc5-1729">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="10bc5-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="10bc5-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10bc5-1730">Az.Aks</span></span>
* <span data-ttu-id="10bc5-1731">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10bc5-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1732">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1733">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="10bc5-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="10bc5-1734">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10bc5-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10bc5-1735">Az.Cdn</span></span>
* <span data-ttu-id="10bc5-1736">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1737">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1738">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="10bc5-1739">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10bc5-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="10bc5-1740">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10bc5-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10bc5-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10bc5-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10bc5-1742">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10bc5-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10bc5-1743">Az.DataFactory</span></span>
* <span data-ttu-id="10bc5-1744">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="10bc5-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-1746">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="10bc5-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="10bc5-1747">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="10bc5-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="10bc5-1748">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1749">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-1750">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10bc5-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1751">Az.KeyVault</span></span>
* <span data-ttu-id="10bc5-1752">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1753">Az.Network</span></span>
* <span data-ttu-id="10bc5-1754">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1755">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1756">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="10bc5-1757">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="10bc5-1758">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="10bc5-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="10bc5-1759">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="10bc5-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="10bc5-1760">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="10bc5-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="10bc5-1761">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="10bc5-1762">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="10bc5-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-1764">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="10bc5-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="10bc5-1765">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1765">Fix some error messages.</span></span>
* <span data-ttu-id="10bc5-1766">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="10bc5-1767">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10bc5-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10bc5-1768">Az.SignalR</span></span>
* <span data-ttu-id="10bc5-1769">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1770">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1771">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10bc5-1772">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="10bc5-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="10bc5-1773">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="10bc5-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="10bc5-1774">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1775">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1776">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10bc5-1777">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="10bc5-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="10bc5-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="10bc5-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="10bc5-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="10bc5-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10bc5-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="10bc5-1781">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1782">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1783">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="10bc5-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10bc5-1784">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="10bc5-1785">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="10bc5-1786">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="10bc5-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10bc5-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1787">Az.Accounts</span></span>
* <span data-ttu-id="10bc5-1788">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="10bc5-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1789">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1790">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="10bc5-1791">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="10bc5-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="10bc5-1792">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-1794">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="10bc5-1795">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="10bc5-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10bc5-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10bc5-1796">Az.EventGrid</span></span>
* <span data-ttu-id="10bc5-1797">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="10bc5-1798">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10bc5-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="10bc5-1799">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10bc5-1800">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="10bc5-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10bc5-1801">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10bc5-1802">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="10bc5-1803">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10bc5-1804">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="10bc5-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10bc5-1805">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10bc5-1806">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="10bc5-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="10bc5-1807">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="10bc5-1808">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10bc5-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1809">Az.IotHub</span></span>
* <span data-ttu-id="10bc5-1810">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="10bc5-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10bc5-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10bc5-1811">Az.LogicApp</span></span>
* <span data-ttu-id="10bc5-1812">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="10bc5-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1813">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1814">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="10bc5-1815">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="10bc5-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="10bc5-1816">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10bc5-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10bc5-1817">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="10bc5-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="10bc5-1818">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="10bc5-1819">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="10bc5-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10bc5-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10bc5-1820">Az.SignalR</span></span>
* <span data-ttu-id="10bc5-1821">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1822">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1823">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10bc5-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1824">Az.Storage</span></span>
* <span data-ttu-id="10bc5-1825">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="10bc5-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="10bc5-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10bc5-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="10bc5-1827">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="10bc5-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="10bc5-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1829">Az.Websites</span></span>
* <span data-ttu-id="10bc5-1830">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="10bc5-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="10bc5-1831">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="10bc5-1832">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="10bc5-1833">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-1833">General</span></span>

- <span data-ttu-id="10bc5-1834">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="10bc5-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="10bc5-1835">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1835">Online help for each module</span></span>
- <span data-ttu-id="10bc5-1836">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="10bc5-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="10bc5-1837">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="10bc5-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="10bc5-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1838">Az.Accounts</span></span>
- <span data-ttu-id="10bc5-1839">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10bc5-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="10bc5-1840">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="10bc5-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10bc5-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="10bc5-1842">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="10bc5-1842">Fixes for #7002</span></span>
- <span data-ttu-id="10bc5-1843">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="10bc5-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10bc5-1844">Az.Batch</span></span>
- <span data-ttu-id="10bc5-1845">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="10bc5-1846">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="10bc5-1847">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="10bc5-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="10bc5-1848">Az.Billing</span></span>
- <span data-ttu-id="10bc5-1849">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="10bc5-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="10bc5-1851">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="10bc5-1852">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="10bc5-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10bc5-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="10bc5-1854">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="10bc5-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="10bc5-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="10bc5-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="10bc5-1856">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="10bc5-1858">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="10bc5-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1859">Az.Monitor</span></span>
- <span data-ttu-id="10bc5-1860">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="10bc5-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10bc5-1861">Az.KeyVault</span></span>
- <span data-ttu-id="10bc5-1862">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="10bc5-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="10bc5-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10bc5-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="10bc5-1864">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="10bc5-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10bc5-1865">Az.Media</span></span>
- <span data-ttu-id="10bc5-1866">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="10bc5-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10bc5-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1867">Az.Network</span></span>
<span data-ttu-id="10bc5-1868">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="10bc5-1869">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="10bc5-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="10bc5-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="10bc5-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="10bc5-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="10bc5-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="10bc5-1878">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="10bc5-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10bc5-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="10bc5-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10bc5-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10bc5-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10bc5-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="10bc5-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="10bc5-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="10bc5-1885">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="10bc5-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="10bc5-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10bc5-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10bc5-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10bc5-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10bc5-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10bc5-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="10bc5-1889">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="10bc5-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="10bc5-1890">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="10bc5-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="10bc5-1892">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="10bc5-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10bc5-1893">Az.Profile</span></span>
- <span data-ttu-id="10bc5-1894">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10bc5-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="10bc5-1896">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="10bc5-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1897">Az.Resources</span></span>
- <span data-ttu-id="10bc5-1898">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10bc5-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="10bc5-1900">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="10bc5-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="10bc5-1901">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="10bc5-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10bc5-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="10bc5-1903">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10bc5-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="10bc5-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1904">Az.Sql</span></span>
- <span data-ttu-id="10bc5-1905">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="10bc5-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="10bc5-1906">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="10bc5-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="10bc5-1907">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="10bc5-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1908">Az.Storage</span></span>
- <span data-ttu-id="10bc5-1909">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10bc5-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1910">Az.Websites</span></span>
- <span data-ttu-id="10bc5-1911">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="10bc5-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="10bc5-1912">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="10bc5-1913">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-1913">General</span></span>

* <span data-ttu-id="10bc5-1914">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="10bc5-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="10bc5-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1915">Az.Compute</span></span>

* <span data-ttu-id="10bc5-1916">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="10bc5-1918">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="10bc5-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="10bc5-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10bc5-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="10bc5-1920">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="10bc5-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="10bc5-1921">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="10bc5-1922">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10bc5-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="10bc5-1924">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="10bc5-1925">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="10bc5-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1926">Az.Resources</span></span>

* <span data-ttu-id="10bc5-1927">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="10bc5-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="10bc5-1928">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="10bc5-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1929">Az.Sql</span></span>

* <span data-ttu-id="10bc5-1930">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="10bc5-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="10bc5-1931">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="10bc5-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="10bc5-1932">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="10bc5-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-1933">Az.Storage</span></span>

* <span data-ttu-id="10bc5-1934">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="10bc5-1935">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="10bc5-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="10bc5-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10bc5-1937">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="10bc5-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="10bc5-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10bc5-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="10bc5-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10bc5-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10bc5-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-1940">Az.Websites</span></span>

* <span data-ttu-id="10bc5-1941">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10bc5-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="10bc5-1942">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="10bc5-1943">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="10bc5-1944">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10bc5-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10bc5-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="10bc5-1946">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="10bc5-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10bc5-1947">Az.Automation</span></span>
* <span data-ttu-id="10bc5-1948">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="10bc5-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="10bc5-1949">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="10bc5-1950">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="10bc5-1951">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="10bc5-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="10bc5-1952">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="10bc5-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="10bc5-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-1953">Az.Compute</span></span>
* <span data-ttu-id="10bc5-1954">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="10bc5-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="10bc5-1955">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10bc5-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="10bc5-1957">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="10bc5-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10bc5-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10bc5-1959">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="10bc5-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10bc5-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-1960">Az.Network</span></span>
* <span data-ttu-id="10bc5-1961">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="10bc5-1962">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="10bc5-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="10bc5-1963">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="10bc5-1964">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10bc5-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="10bc5-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10bc5-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10bc5-1966">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="10bc5-1967">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="10bc5-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="10bc5-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="10bc5-1969">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10bc5-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="10bc5-1970">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="10bc5-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="10bc5-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10bc5-1971">Az.Relay</span></span>
* <span data-ttu-id="10bc5-1972">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="10bc5-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-1973">Az.Resources</span></span>
* <span data-ttu-id="10bc5-1974">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="10bc5-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="10bc5-1975">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="10bc5-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="10bc5-1976">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="10bc5-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10bc5-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-1978">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="10bc5-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="10bc5-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-1979">Az.Sql</span></span>
* <span data-ttu-id="10bc5-1980">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="10bc5-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="10bc5-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10bc5-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10bc5-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10bc5-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10bc5-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10bc5-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10bc5-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10bc5-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10bc5-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10bc5-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10bc5-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10bc5-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10bc5-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="10bc5-1989">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="10bc5-1990">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="10bc5-1991">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="10bc5-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10bc5-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10bc5-1994">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="10bc5-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="10bc5-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="10bc5-1996">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="10bc5-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="10bc5-1997">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10bc5-1998">Geral</span><span class="sxs-lookup"><span data-stu-id="10bc5-1998">General</span></span>
* <span data-ttu-id="10bc5-1999">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="10bc5-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="10bc5-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2000">Az.Profile</span></span>
* <span data-ttu-id="10bc5-2001">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10bc5-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="10bc5-2002">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="10bc5-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="10bc5-2003">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10bc5-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="10bc5-2004">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="10bc5-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="10bc5-2005">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="10bc5-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="10bc5-2006">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="10bc5-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="10bc5-2007">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="10bc5-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-2009">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-2010">Az.Compute</span></span>
* <span data-ttu-id="10bc5-2011">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="10bc5-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="10bc5-2012">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="10bc5-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="10bc5-2013">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-2015">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="10bc5-2016">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="10bc5-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="10bc5-2017">Az.Insights</span></span>
* <span data-ttu-id="10bc5-2018">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="10bc5-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="10bc5-2019">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="10bc5-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="10bc5-2020">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="10bc5-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="10bc5-2021">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="10bc5-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-2022">Az.Network</span></span>
* <span data-ttu-id="10bc5-2023">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="10bc5-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="10bc5-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="10bc5-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="10bc5-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10bc5-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="10bc5-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="10bc5-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="10bc5-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="10bc5-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10bc5-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10bc5-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10bc5-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="10bc5-2031">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="10bc5-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-2032">Az.Resources</span></span>
* <span data-ttu-id="10bc5-2033">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="10bc5-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="10bc5-2034">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="10bc5-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10bc5-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10bc5-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="10bc5-2036">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10bc5-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10bc5-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="10bc5-2038">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="10bc5-2039">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="10bc5-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="10bc5-2040">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="10bc5-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="10bc5-2041">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="10bc5-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="10bc5-2042">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="10bc5-2043">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="10bc5-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2044">Az.Profile</span></span>
* <span data-ttu-id="10bc5-2045">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="10bc5-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="10bc5-2046">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10bc5-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-2047">Az.Compute</span></span>
* <span data-ttu-id="10bc5-2048">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="10bc5-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="10bc5-2049">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10bc5-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10bc5-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="10bc5-2051">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="10bc5-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="10bc5-2052">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="10bc5-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10bc5-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10bc5-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-2056">Az.Network</span></span>
* <span data-ttu-id="10bc5-2057">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="10bc5-2058">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-2059">Az.Resources</span></span>
* <span data-ttu-id="10bc5-2060">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="10bc5-2061">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="10bc5-2062">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="10bc5-2063">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="10bc5-2063">Azure.Storage</span></span>
* <span data-ttu-id="10bc5-2064">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="10bc5-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="10bc5-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="10bc5-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10bc5-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10bc5-2067">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="10bc5-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="10bc5-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="10bc5-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10bc5-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="10bc5-2070">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10bc5-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10bc5-2071">Az.Compute</span></span>
* <span data-ttu-id="10bc5-2072">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="10bc5-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="10bc5-2073">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="10bc5-2074">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="10bc5-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="10bc5-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10bc5-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="10bc5-2076">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10bc5-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10bc5-2077">Az.Network</span></span>
* <span data-ttu-id="10bc5-2078">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="10bc5-2079">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="10bc5-2079">new cmdlets added</span></span>
    - <span data-ttu-id="10bc5-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="10bc5-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="10bc5-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="10bc5-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10bc5-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="10bc5-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="10bc5-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="10bc5-2086">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="10bc5-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="10bc5-2087">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10bc5-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="10bc5-2088">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="10bc5-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10bc5-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10bc5-2089">Az.RedisCache</span></span>
* <span data-ttu-id="10bc5-2090">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="10bc5-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="10bc5-2091">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="10bc5-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="10bc5-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10bc5-2092">Az.Resources</span></span>
* <span data-ttu-id="10bc5-2093">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10bc5-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10bc5-2094">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="10bc5-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="10bc5-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10bc5-2095">Az.Sql</span></span>
* <span data-ttu-id="10bc5-2096">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="10bc5-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10bc5-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10bc5-2097">Az.Websites</span></span>
* <span data-ttu-id="10bc5-2098">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="10bc5-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="10bc5-2099">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="10bc5-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="10bc5-2100">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="10bc5-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="10bc5-2101">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="10bc5-2101">Initial Release</span></span>
